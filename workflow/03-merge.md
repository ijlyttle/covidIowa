Merge data
================
Compiled at 2021-02-28 04:00:59 UTC

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

    ## Rows: 27,307
    ## Columns: 7
    ## Delimiter: ","
    ## chr  [1]: county
    ## dbl  [5]: fips, tests, cases, recovered, deaths
    ## date [1]: date
    ## 
    ## Use `spec()` to retrieve the guessed column specification
    ## Pass a specification to the `col_types` argument to quiet this message

``` r
tail(iowa_county_data)
```

    ## # A tibble: 6 x 7
    ##   date        fips county    tests cases recovered deaths
    ##   <date>     <dbl> <chr>     <dbl> <dbl>     <dbl>  <dbl>
    ## 1 2021-02-27 19071 Fremont    2488   554       533      9
    ## 2 2021-02-27 19177 Van Buren  2569   535       502     18
    ## 3 2021-02-27 19159 Ringgold   2246   500       456     20
    ## 4 2021-02-27 19009 Audubon    2448   469       423      9
    ## 5 2021-02-27 19185 Wayne      2081   449       404     21
    ## 6 2021-02-27 19003 Adams      1494   317       307      4

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
    ## 1 iowa_county_data.csv file        1.05M 2021-02-28 04:01:25