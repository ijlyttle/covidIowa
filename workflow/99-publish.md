99-publish
================
Compiled at 2021-02-28 04:01:29 UTC

``` r
here::i_am(paste0(params$name, ".Rmd"), uuid = "da2d40a5-231f-404f-96ad-f86272f58669")
```

The purpose of this document is …

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
  path_source("04-explore", "iowa_county_cases_week_current.csv"),
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

    ## # A tibble: 6 x 4
    ##   path                               type         size modification_time  
    ##   <fs::path>                         <fct> <fs::bytes> <dttm>             
    ## 1 iowa_cases.png                     file      204.03K 2021-02-28 04:01:29
    ## 2 iowa_cases_week.csv                file       14.72K 2021-02-28 04:01:29
    ## 3 iowa_change.png                    file      180.65K 2021-02-28 04:01:29
    ## 4 iowa_county_cases_week_current.csv file        6.93K 2021-02-28 04:01:29
    ## 5 iowa_county_data.csv               file        1.05M 2021-02-28 04:01:29
    ## 6 iowa_county_meta.csv               file        6.62K 2021-02-28 04:01:29