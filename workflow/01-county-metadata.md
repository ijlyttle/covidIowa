County metadata
================
Compiled at 2021-06-16 17:11:41 UTC

``` r
here::i_am(paste0(params$name, ".Rmd"), uuid = "cee9aa30-7c5a-42d3-80bc-621c4467656f")
```

The purpose of this document is to write out a CSV file that contains
county population.

``` r
library("conflicted")
library("readxl")
library("dplyr")
library("stringr")
library("forcats")
library("readr")
library("ggplot2")
library("maps")

conflict_prefer("filter", "dplyr")
```

    ## [conflicted] Will prefer dplyr::filter over any other package

``` r
# create or *empty* the target directory, used to write this file's data: 
projthis::proj_create_dir_target(params$name, clean = TRUE)

# function to get path to target directory: path_target("sample.csv")
path_target <- projthis::proj_path_target(params$name)

# function to get path to previous data: path_source("00-import", "sample.csv")
path_source <- projthis::proj_path_source(params$name)
```

## Tasks

Let’s do this using a pipe:

``` r
iowa_county_population <-
  read_xls(
    path = path_source("00-import", "county-population", "iowa-county-population.xls"), 
    sheet = "Counties", 
    range = "A7:M107"
  ) %>%
  transmute(
    fips = Fips,
    county = str_replace(Area, " County, Iowa", ""),
    population = `2019`
  ) %>%
  filter(fips > 19) %>%
  arrange(population) %>%
  mutate(
    cumulative_population = cumsum(population),
    quantile_population = cumulative_population/max(cumulative_population),
    population_group = cut(
      quantile_population, 
      breaks = c(0, 0.25, 0.50, 0.78, 1),
      labels = c("small", "mid-small", "mid-large", "large")
    ),
    population_group = fct_rev(population_group)
  ) %>%
  arrange(desc(cumulative_population)) %>%
  print()
```

    ## # A tibble: 99 x 6
    ##     fips county   population cumulative_popul… quantile_popula… population_group
    ##    <dbl> <chr>         <dbl>             <dbl>            <dbl> <fct>           
    ##  1 19153 Polk         490161           3155070            1     large           
    ##  2 19113 Linn         226706           2664909            0.845 large           
    ##  3 19163 Scott        172943           2438203            0.773 mid-large       
    ##  4 19103 Johnson      151140           2265260            0.718 mid-large       
    ##  5 19013 Black H…     131228           2114120            0.670 mid-large       
    ##  6 19193 Woodbury     103107           1982892            0.628 mid-large       
    ##  7 19061 Dubuque       97311           1879785            0.596 mid-large       
    ##  8 19169 Story         97117           1782474            0.565 mid-large       
    ##  9 19049 Dallas        93453           1685357            0.534 mid-large       
    ## 10 19155 Pottawa…      93206           1591904            0.505 mid-large       
    ## # … with 89 more rows

We also want to compute the approximate centers of the counties (trick I
picked up from Heike Hofmann).

``` r
map_iowa_county <-
  map_data("county") %>%
  filter(region == "iowa") %>%
  group_by(county = subregion) %>%
  summarise(
    lat = (max(lat) + min(lat)) / 2,
    lon =  (max(long) + min(long)) / 2
  ) %>%
  mutate(
    abbreviation = str_to_upper(county) %>% str_sub(1, 3),
    county = str_to_title(county),
    county = ifelse(county == "Obrien", "O'Brien", county)
  ) %>%
  glimpse()
```

    ## Rows: 99
    ## Columns: 4
    ## $ county       <chr> "Adair", "Adams", "Allamakee", "Appanoose", "Audubon", "B…
    ## $ lat          <dbl> 41.33318, 41.03237, 43.29556, 40.75449, 41.68554, 42.0866…
    ## $ lon          <dbl> -94.47787, -94.70992, -91.33520, -92.86787, -94.90759, -9…
    ## $ abbreviation <chr> "ADA", "ADA", "ALL", "APP", "AUD", "BEN", "BLA", "BOO", "…

``` r
iowa_county_meta <-
  iowa_county_population %>%
  select(fips, county, population, population_group) %>%
  left_join(
    map_iowa_county, 
    by = "county"
  ) %>%
  select(fips, county, abbreviation, lon, lat, everything()) %>%
  glimpse()
```

    ## Rows: 99
    ## Columns: 7
    ## $ fips             <dbl> 19153, 19113, 19163, 19103, 19013, 19193, 19061, 1916…
    ## $ county           <chr> "Polk", "Linn", "Scott", "Johnson", "Black Hawk", "Wo…
    ## $ abbreviation     <chr> "POL", "LIN", "SCO", "JOH", "BLA", "WOO", "DUB", "STO…
    ## $ lon              <dbl> -93.57833, -91.58730, -90.60182, -91.58730, -92.30637…
    ## $ lat              <dbl> 41.67695, 42.08661, 41.62825, 41.64830, 42.47336, 42.…
    ## $ population       <dbl> 490161, 226706, 172943, 151140, 131228, 103107, 97311…
    ## $ population_group <fct> large, large, mid-large, mid-large, mid-large, mid-la…

Let’s write this out:

``` r
write_csv(
  iowa_county_meta,
  path_target("iowa_county_meta.csv")
)
```

## Files written

These files have been written to the target directory,
`data/01-county-metadata`:

``` r
projthis::proj_dir_info(path_target())
```

    ## # A tibble: 1 x 4
    ##   path                 type         size modification_time  
    ##   <fs::path>           <fct> <fs::bytes> <dttm>             
    ## 1 iowa_county_meta.csv file        6.62K 2021-06-16 17:11:42
