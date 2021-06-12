Compiled at 2021-06-12 23:52:45 UTC

<!-- README.md is generated from README.Rmd. Please edit that file -->

# covidIowa

<!-- badges: start -->

<!-- badges: end -->

The goal of this repository is to give a county-level summary of
COVID-19 cases in Iowa. The data is taken from a series of daily
snapshots of the [accessibility
page](https://coronavirus.iowa.gov/pages/access) provided by the Iowa
Department of Public Health.

If you want to work with the data yourself, all the code I use is
published this repository, check out the [`workflow`](workflow)
directory. Processed datasets are also available here:

  - [`iowa_county_meta.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_meta.csv):
    county metadata, things like estimated 2019 population from
    [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
    at Iowa State University.

  - [`iowa_county_data.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_data.csv):
    daily numbers by county from IDPH, going back to 2020-05-25.

  - [`iowa_county_cases_week.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_data.csv):
    In addition to county metadata, total positive-tests (and per 100k),
    one week average of daily positive-tests (and per 100k), and
    week-over-week change in positive tests (as a ratio).

  - [`iowa_cases_week.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_cases_week.csv):
    Similar to `iowa_county_cases_week.csv`, but aggregated for the
    entire state.

## Plots

![](workflow/data/99-publish/iowa_cases.png)

![](workflow/data/99-publish/iowa_change.png)

## Tables as of 2021-06-12

As of 2021-06-12, IPDH is reporting 127 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   14.7 |                             3.0 |                 11.1% |
|          Linn |                    8.3 |                             3.7 |               \-16.7% |
|         Scott |                    3.3 |                             1.9 |               \-51.6% |
|       Johnson |                    2.7 |                             1.8 |               \-23.5% |
|    Black Hawk |                   11.7 |                             8.9 |                 36.9% |
|      Woodbury |                    2.3 |                             2.2 |                  9.5% |
|       Dubuque |                    3.0 |                             3.1 |               \-22.2% |
|         Story |                    1.3 |                             1.3 |               \-15.8% |
|        Dallas |                    2.4 |                             2.6 |               \-20.0% |
| Pottawattamie |                    2.4 |                             2.6 |                \-4.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    1.0 |                            18.2 |                 16.7% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
| Black Hawk |                   11.7 |                             8.9 |                 36.9% |
|     Taylor |                    0.4 |                             7.0 |                 25.0% |
|   Hamilton |                    1.0 |                             6.8 |                 55.5% |
|       Page |                    1.0 |                             6.6 |                 27.3% |
|     Louisa |                    0.6 |                             5.2 |                 22.2% |
|   Buchanan |                    1.0 |                             4.7 |                 55.5% |
|        Lee |                    1.6 |                             4.7 |                \-5.3% |
|     Grundy |                    0.6 |                             4.7 |                 37.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Carroll |                    0.1 |                             0.7 |                 60.1% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
|   Buchanan |                    1.0 |                             4.7 |                 55.5% |
|   Hamilton |                    1.0 |                             6.8 |                 55.5% |
|     Shelby |                    0.3 |                             2.5 |                 50.1% |
|    Wapello |                    0.9 |                             2.5 |                 44.4% |
|     Jasper |                    0.4 |                             1.2 |                 42.9% |
|     Warren |                    2.0 |                             3.9 |                 40.0% |
|     Grundy |                    0.6 |                             4.7 |                 37.4% |
| Black Hawk |                   11.7 |                             8.9 |                 36.9% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Henry |                  \-0.3 |                           \-1.4 |               \-68.8% |
|      Scott |                    3.3 |                             1.9 |               \-51.6% |
|   Marshall |                    0.0 |                             0.0 |               \-50.0% |
| Des Moines |                    1.1 |                             2.9 |               \-50.0% |
|     Wright |                    0.0 |                             0.0 |               \-50.0% |
|      Davis |                    0.1 |                             1.6 |               \-46.7% |
|   Crawford |                  \-0.1 |                           \-0.8 |               \-45.4% |
|  Winnebago |                    0.1 |                             1.4 |               \-42.8% |
|      Jones |                    0.0 |                             0.0 |               \-41.7% |
|    Madison |                    0.1 |                             0.9 |               \-38.4% |
