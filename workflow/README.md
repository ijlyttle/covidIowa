Workflow
================
Compiled at 2021-09-02 17:32:38 UTC

``` r
here::i_am("README.Rmd", uuid = "c0fce685-fcbc-40c7-97d2-f9ba37fdaac5")

# function to get path to previous data: path_source("99-publish", "sample.csv")
path_source <- projthis::proj_path_source("README")
```

In this workflow, we will:

  - [import](00-import.md):
      - daily snapshots of the [IDPH accessibility
        page](https://coronavirus.iowa.gov/pages/access)
      - county population from
        [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
        at Iowa State University.
  - extract the [county metadata](01-county-metadata.md)
  - [scrape](02-scrape-idph.md) the data from the IDPH shapshots
  - [merge](03-merge.md) IDPH data
  - [explore](04-explore.md) the data
  - [publish](99-publish.md) the data and the plots

<!-- end list -->

``` r
library("conflicted")
```
