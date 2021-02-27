Import data
================
Compiled at 2021-02-27 17:49:30 UTC

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

The first task is to set up some decide on “today’s” file-name:

``` r
html_file <- path_target(glue("access-{today(tz = 'America/Chicago')}.html"))
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
location on your computer (on mine, it is
`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"`). The
**crrri** package uses the environment variable `HEADLESS_CHROME` to
look for a default value.

In the future, it may be interesting for this step (downloading the html
file) to be split into its own Action (using JS).

``` r
chrome <- Chrome$new(bin = pagedown::find_chrome())
```

    ## Running '/Applications/Google Chrome.app/Contents/MacOS/Google Chrome' \
    ##   --no-first-run --headless \
    ##   '--user-data-dir=/Users/sesa19001/Library/Application Support/r-crrri/chrome-data-dir-jpgriksf' \
    ##   '--remote-debugging-port=9222' \
    ##   '--proxy-server=http://force-proxy-eur.pac.schneider-electric.com:80' \
    ##   '--proxy-bypass-list=localhost;127.0.0.1;github.schneider-electric.com;repo.continuum.io;github-development.schneider-electric.com'

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

## Files written

These files have been written to the target directory, `data/00-import`:

``` r
projthis::proj_dir_info(path_target()) %>% 
  arrange(desc(modification_time)) # show most-recent first
```

    ## # A tibble: 278 x 4
    ##    path                   type         size modification_time  
    ##    <fs::path>             <fct> <fs::bytes> <dttm>             
    ##  1 access-2021-02-27.html file        5.39K 2021-02-27 17:49:47
    ##  2 access-2021-02-26.html file      489.68K 2021-02-27 16:23:59
    ##  3 access-2021-02-25.html file      489.68K 2021-02-27 16:23:59
    ##  4 access-2021-02-24.html file      489.68K 2021-02-27 16:23:59
    ##  5 access-2021-02-23.html file      489.68K 2021-02-27 16:23:59
    ##  6 access-2021-02-22.html file      491.79K 2021-02-27 16:23:59
    ##  7 access-2021-02-21.html file      491.79K 2021-02-27 16:23:59
    ##  8 access-2021-02-20.html file      491.79K 2021-02-27 16:23:59
    ##  9 access-2021-02-19.html file      491.79K 2021-02-27 16:23:59
    ## 10 access-2021-02-18.html file      494.27K 2021-02-27 16:23:59
    ## # … with 268 more rows
