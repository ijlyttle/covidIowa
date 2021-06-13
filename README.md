Compiled at 2021-06-13 20:14:26 UTC

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

## Tables as of 2021-06-13

As of 2021-06-13, IPDH is reporting 55 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   12.7 |                             2.6 |                \-5.0% |
|          Linn |                    8.0 |                             3.5 |               \-29.2% |
|         Scott |                    2.4 |                             1.4 |               \-58.6% |
|       Johnson |                    2.1 |                             1.4 |               \-33.3% |
|    Black Hawk |                   12.9 |                             9.8 |                 42.6% |
|      Woodbury |                    1.7 |                             1.7 |                \-5.0% |
|       Dubuque |                    3.0 |                             3.1 |               \-22.2% |
|         Story |                    1.1 |                             1.2 |               \-25.0% |
|        Dallas |                    1.9 |                             2.0 |               \-37.5% |
| Pottawattamie |                    2.1 |                             2.3 |               \-26.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |                \-7.7% |
|    Ringgold |                    0.6 |                            11.7 |                 57.1% |
|  Black Hawk |                   12.9 |                             9.8 |                 42.6% |
|      Shelby |                    0.9 |                             7.5 |                225.2% |
| Cerro Gordo |                    3.0 |                             7.1 |                 40.0% |
|      Taylor |                    0.4 |                             7.0 |                 42.9% |
|    Hamilton |                    0.9 |                             5.8 |                 44.4% |
|        Page |                    0.9 |                             5.7 |                  8.3% |
|      Louisa |                    0.6 |                             5.2 |                 83.3% |
|    Buchanan |                    1.0 |                             4.7 |                 75.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Shelby |                    0.9 |                             7.5 |                225.2% |
|     Louisa |                    0.6 |                             5.2 |                 83.3% |
|   Buchanan |                    1.0 |                             4.7 |                 75.0% |
|      Cedar |                    0.9 |                             4.6 |                 62.5% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
|       Iowa |                    0.3 |                             1.8 |                 50.1% |
|   Hamilton |                    0.9 |                             5.8 |                 44.4% |
|     Jasper |                    0.4 |                             1.2 |                 42.9% |
|     Taylor |                    0.4 |                             7.0 |                 42.9% |
| Black Hawk |                   12.9 |                             9.8 |                 42.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Scott |                    2.4 |                             1.4 |               \-58.6% |
| Des Moines |                    0.6 |                             1.5 |               \-57.7% |
|      Henry |                  \-0.1 |                           \-0.7 |               \-57.2% |
|    Madison |                  \-0.1 |                           \-0.9 |               \-57.2% |
|    O’Brien |                  \-0.4 |                           \-3.1 |               \-50.0% |
|  Winnebago |                    0.1 |                             1.4 |               \-42.8% |
|   Franklin |                    0.1 |                             1.4 |               \-42.8% |
| Washington |                    0.6 |                             2.6 |               \-42.1% |
|   Cherokee |                  \-0.1 |                           \-1.3 |               \-40.0% |
|  Muscatine |                    0.9 |                             2.0 |               \-38.1% |
