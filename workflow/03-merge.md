Merge data
================
Compiled at 2021-06-23 23:51:05 UTC

``` r
here::i_am(paste0(params$name, ".Rmd"), uuid = "395c01d6-11f2-4832-9c79-3089737223b8")
```

The purpose of this document is to merge the daily datasets.

``` r
library("conflicted")
library("fs")
library("readr")
library("purrr")
library("dplyr")
library("vroom")
```

``` r
# create or *empty* the target directory, used to write this file's data: 
projthis::proj_create_dir_target(params$name, clean = TRUE)

# function to get path to target directory: path_target("sample.csv")
path_target <- projthis::proj_path_target(params$name)

# function to get path to previous data: path_source("00-import", "sample.csv")
path_source <- projthis::proj_path_source(params$name)
```

## Tasks

Let’s get the names of all the valid CSV files:

``` r
files <- 
  fs::dir_ls(
    path_source("02-scrape-idph"), 
    regexp = "access-\\d{4}-\\d{2}-\\d{2}\\.csv"
  )
```

Let’s read them in:

``` r
iowa_county_data <- 
  vroom(files) %>%
  arrange(date)
```

    ## Rows: 38607 Columns: 7

    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr  (1): county
    ## dbl  (5): fips, tests, cases, recovered, deaths
    ## date (1): date

    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
tail(iowa_county_data)
```

    ## # A tibble: 6 x 7
    ##   date        fips county    tests cases recovered deaths
    ##   <date>     <dbl> <chr>     <dbl> <dbl>     <dbl>  <dbl>
    ## 1 2021-06-23 19053 Decatur    3780   616       608      9
    ## 2 2021-06-23 19177 Van Buren  2957   564       544     18
    ## 3 2021-06-23 19159 Ringgold   2534   564       540     24
    ## 4 2021-06-23 19185 Wayne      2696   544       520     23
    ## 5 2021-06-23 19009 Audubon    2894   535       506     11
    ## 6 2021-06-23 19003 Adams      1697   345       340      4

Let’s write it out:

``` r
write_csv(iowa_county_data, path_target("iowa_county_data.csv"))
```

## Files written

These files have been written to the target directory, `data/03-merge`:

``` r
projthis::proj_dir_info(path_target())
```

    ## # A tibble: 1 x 4
    ##   path                 type         size modification_time  
    ##   <fs::path>           <fct> <fs::bytes> <dttm>             
    ## 1 iowa_county_data.csv file        1.52M 2021-06-23 23:51:55
