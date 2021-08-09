99-publish
================
Compiled at 2021-08-09 20:26:29 UTC

``` r
here::i_am(paste0(params$name, ".Rmd"), uuid = "da2d40a5-231f-404f-96ad-f86272f58669")
```

The purpose of this document is to make data and images available.

``` r
library("conflicted")
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

This will be just copying files from earlier in the workflow:

``` r
fs::file_copy(
  path_source("01-county-metadata", "iowa_county_meta.csv"),
  path_target()
)
```

``` r
fs::file_copy(
  path_source("03-merge", "iowa_county_data.csv"),
  path_target()
)
```

``` r
fs::file_copy(
  path_source("04-explore", "iowa_county_cases_week.csv"),
  path_target()
)
```

``` r
fs::file_copy(
  path_source("04-explore", "iowa_cases_week.csv"),
  path_target()
)
```

``` r
fs::file_copy(
  path_source("04-explore", "iowa_cases.png"),
  path_target()
)
```

``` r
fs::file_copy(
  path_source("04-explore", "iowa_change.png"),
  path_target()
)
```

## Files written

These files have been written to the target directory,
`data/99-publish`:

``` r
projthis::proj_dir_info(path_target())
```

    ## # A tibble: 6 × 4
    ##   path                       type         size modification_time  
    ##   <fs::path>                 <fct> <fs::bytes> <dttm>             
    ## 1 iowa_cases.png             file      201.99K 2021-08-09 20:26:30
    ## 2 iowa_cases_week.csv        file        22.5K 2021-08-09 20:26:30
    ## 3 iowa_change.png            file      194.24K 2021-08-09 20:26:30
    ## 4 iowa_county_cases_week.csv file        2.71M 2021-08-09 20:26:30
    ## 5 iowa_county_data.csv       file        1.64M 2021-08-09 20:26:30
    ## 6 iowa_county_meta.csv       file        6.62K 2021-08-09 20:26:30
