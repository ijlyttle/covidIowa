Import data
================
Compiled at 2021-07-14 23:52:45 UTC

``` r
here::i_am(paste0(params$name, ".Rmd"), uuid = "0deed706-3efe-402b-b827-b58e9bb3e976")
```

The purpose of this document is to collect all the data we need, in raw
form.

``` r
library("conflicted")
library("fs")
library("glue")
library("crrri")
library("dplyr")
library("lubridate")
```

We are going to seed the dataset using some HTML files I had previously
downloaded, so we will not start the target directory in a `clean` state
every time we run it.

``` r
# create or *empty* the target directory, used to write this file's data: 
projthis::proj_create_dir_target(params$name, clean = FALSE)

# function to get path to target directory: path_target("sample.csv")
path_target <- projthis::proj_path_target(params$name)

# function to get path to previous data: path_source("00-import", "sample.csv")
path_source <- projthis::proj_path_source(params$name)
```

## Tasks

### HTML files

These are daily snapshots from the Iowa Department of Public Health.

``` r
html_file <- 
  path_target("idph-html", glue("access-{today(tz = 'America/Chicago')}.html"))
```

We are going to use [rvest](https://rvest.tidyverse.org/) to page, but
there’s a problem. The page is not a static HTML site; the data we want
is injected into the site using JavaScript. This means that **rvest**
would be looking for the css tags in a document that does not have the
data table.

We need another tool for the toolbox:
[crrri](https://rlesur.github.io/crrri) - a package written by Romain
Lesur and Christophe Dervieux - which will let us build the page
locally, using Chrome. Then we will scrape it, using our local copy of
the page.

The **crrri** package is not on CRAN, and it requires that you have
Chrome installed on your computer, so that it can call it in the
background. To run Chrome, the **crrri** package will need to know where
to *find* Chrome. You can use `pagedown::find_chrome()` to find the
location on your computer (on mine, it is `"/Applications/Google
Chrome.app/Contents/MacOS/Google Chrome"`). The **crrri** package uses
the environment variable `HEADLESS_CHROME` to look for a default value.

In the future, it may be interesting for this step (downloading the html
file) to be split into its own Action (using JS).

``` r
chrome <- Chrome$new(bin = pagedown::find_chrome())
```

    ## Running '/Applications/Google Chrome.app/Contents/MacOS/Google Chrome' \
    ##   --no-first-run --headless \
    ##   '--user-data-dir=/Users/runner/Library/Application Support/r-crrri/chrome-data-dir-orwjiydg' \
    ##   '--remote-debugging-port=9222'

``` r
client <- chrome$connect()
```

``` r
dump_DOM <- function(client, url, html_file) {
  Network <- client$Network
  Page <- client$Page
  Runtime <- client$Runtime
  Network$enable() %...>%
  { Page$enable() } %...>%
  { Network$setCacheDisabled(cacheDisabled = TRUE) } %...>% 
  { Page$navigate(url = url) } %...>%
  { Page$loadEventFired() } %...>% {
    Sys.sleep(10) # hacky - wait for a certain event, instead
  } %...>% { 
    Runtime$evaluate(
      expression = 'document.documentElement.outerHTML'
    ) 
  } %...>% {
    writeLines(c(.$result$value, "\n"), con = html_file) 
  } %>%
  finally(
    ~ client$disconnect()
  ) %...!% {
    cat("Error:", .$message, "\n")
  }
}
```

``` r
hold(
  client %...>% dump_DOM(params$url_access, html_file)  
)
```

    ## NULL

``` r
chrome$close()
```

### County population

This is an excel sheet offered by Iowa State University:

``` r
file_population <- 
  path_target("county-population", "iowa-county-population.xls")

if (!file_exists(file_population)) {
  download.file(params$url_population, destfile = file_population)
}
```

## Files written

These files have been written to the target directory, `data/00-import`:

``` r
projthis::proj_dir_info(path_target()) 
```

    ## # A tibble: 2 x 4
    ##   path              type             size modification_time  
    ##   <fs::path>        <fct>     <fs::bytes> <dttm>             
    ## 1 county-population directory          96 2021-07-14 23:50:17
    ## 2 idph-html         directory         13K 2021-07-14 23:50:18

``` r
projthis::proj_dir_info(path_target("county-population")) 
```

    ## # A tibble: 1 x 4
    ##   path                       type         size modification_time  
    ##   <fs::path>                 <fct> <fs::bytes> <dttm>             
    ## 1 iowa-county-population.xls file         230K 2021-07-14 23:50:17

``` r
projthis::proj_dir_info(path_target("idph-html")) %>% 
  arrange(desc(path)) # show most-recent first
```

    ## # A tibble: 415 x 4
    ##    path                   type         size modification_time  
    ##    <fs::path>             <fct> <fs::bytes> <dttm>             
    ##  1 access-2021-07-14.html file         534K 2021-07-14 23:53:01
    ##  2 access-2021-07-13.html file         534K 2021-07-14 23:50:18
    ##  3 access-2021-07-12.html file         534K 2021-07-14 23:50:18
    ##  4 access-2021-07-11.html file         534K 2021-07-14 23:50:18
    ##  5 access-2021-07-10.html file         534K 2021-07-14 23:50:18
    ##  6 access-2021-07-09.html file         534K 2021-07-14 23:50:18
    ##  7 access-2021-07-08.html file         535K 2021-07-14 23:50:18
    ##  8 access-2021-07-07.html file         535K 2021-07-14 23:50:18
    ##  9 access-2021-07-06.html file         538K 2021-07-14 23:50:18
    ## 10 access-2021-07-05.html file         537K 2021-07-14 23:50:18
    ## # … with 405 more rows
