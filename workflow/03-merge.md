Merge data
================
Compiled at 2021-07-15 20:15:46 UTC

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

    ## Rows: 40808 Columns: 7

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
    ##   date        fips county                tests cases recovered deaths
    ##   <date>     <dbl> <chr>                 <dbl> <dbl>     <dbl>  <dbl>
    ## 1 2021-07-15 19177 Van Buren              3002   567       550     18
    ## 2 2021-07-15 19159 Ringgold               2563   564       536     24
    ## 3 2021-07-15 19185 Wayne                  2753   561       528     23
    ## 4 2021-07-15 19009 Audubon                2915   529       514     12
    ## 5 2021-07-15 19003 Adams                  1714   346       333      4
    ## 6 2021-07-15    NA Pending Investigation  3376     8         4      0

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
    ## 1 iowa_county_data.csv file        1.61M 2021-07-15 20:16:25
