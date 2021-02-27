Workflow
================
Compiled at 2021-02-27 21:13:50 UTC

``` r
here::i_am("README.Rmd", uuid = "c0fce685-fcbc-40c7-97d2-f9ba37fdaac5")

# function to get path to previous data: path_source("99-publish", "sample.csv")
path_source <- projthis::proj_path_source("README")
```

In this workflow, we will:

  - [import](00-import.md):
      - daily snapshots of the [IDPH accessibility
        page](https://coronavirus.iowa.gov/pages/access)
      - county metadata
  - scrape the data from the shapshots
  - extract the county metadata
  - merge the data into various forms
  - plot the data
  - publish the data and the plots

<!-- end list -->

``` r
library("conflicted")
```
