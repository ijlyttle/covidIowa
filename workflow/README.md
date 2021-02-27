Workflow
================
Compiled at 2021-02-27 16:19:45 UTC

``` r
here::i_am("README.Rmd", uuid = "c0fce685-fcbc-40c7-97d2-f9ba37fdaac5")

# function to get path to previous data: path_source("99-publish", "sample.csv")
path_source <- projthis::proj_path_source("README")
```

In this workflow, we will:

-   download:
    -   a copy of the [IDPH accessibility
        page](https://coronavirus.iowa.gov/pages/access)
    -   county metadata
-   scrape the data from the pages
-   merge the data into various forms
-   plot the data
-   publish the data and the plots

``` r
library("conflicted")
```
