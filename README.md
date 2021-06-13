Compiled at 2021-06-13 16:59:50 UTC

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

As of 2021-06-12, IPDH is reporting 182 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-12 |                   89.7 |                             2.8 |               \-11.6% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   15.0 |                             3.1 |                 13.1% |
|          Linn |                    9.3 |                             4.1 |                \-7.7% |
|         Scott |                    3.4 |                             2.0 |               \-50.0% |
|       Johnson |                    2.7 |                             1.8 |               \-23.5% |
|    Black Hawk |                   13.6 |                            10.3 |                 56.9% |
|      Woodbury |                    2.1 |                             2.1 |                  4.8% |
|       Dubuque |                    3.1 |                             3.2 |               \-19.4% |
|         Story |                    1.4 |                             1.5 |               \-10.5% |
|        Dallas |                    2.4 |                             2.6 |               \-20.0% |
| Pottawattamie |                    2.7 |                             2.9 |                  4.0% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.9 |                            15.6 |                  8.3% |
|    Ringgold |                    0.6 |                            11.7 |                 57.1% |
|  Black Hawk |                   13.6 |                            10.3 |                 56.9% |
| Cerro Gordo |                    3.1 |                             7.4 |                 45.0% |
|      Taylor |                    0.4 |                             7.0 |                 25.0% |
|    Hamilton |                    1.0 |                             6.8 |                 55.5% |
|        Page |                    1.0 |                             6.6 |                 27.3% |
|      Shelby |                    0.7 |                             6.2 |                100.0% |
|       Floyd |                    0.9 |                             5.5 |                 44.4% |
|      Warren |                    2.7 |                             5.3 |                 73.3% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Shelby |                    0.7 |                             6.2 |                100.0% |
|      Warren |                    2.7 |                             5.3 |                 73.3% |
|     Carroll |                    0.1 |                             0.7 |                 60.1% |
|      Jasper |                    0.6 |                             1.5 |                 57.1% |
|    Ringgold |                    0.6 |                            11.7 |                 57.1% |
|  Black Hawk |                   13.6 |                            10.3 |                 56.9% |
|     Wapello |                    1.0 |                             2.9 |                 55.5% |
|    Buchanan |                    1.0 |                             4.7 |                 55.5% |
|    Hamilton |                    1.0 |                             6.8 |                 55.5% |
| Cerro Gordo |                    3.1 |                             7.4 |                 45.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Henry |                  \-0.1 |                           \-0.7 |               \-62.5% |
|      Scott |                    3.4 |                             2.0 |               \-50.0% |
|   Marshall |                    0.0 |                             0.0 |               \-50.0% |
| Des Moines |                    1.1 |                             2.9 |               \-50.0% |
|      Davis |                    0.1 |                             1.6 |               \-46.7% |
|    Madison |                    0.0 |                             0.0 |               \-46.1% |
|   Crawford |                  \-0.1 |                           \-0.8 |               \-45.4% |
|      Boone |                    0.1 |                             0.5 |               \-42.8% |
|      Jones |                    0.0 |                             0.0 |               \-41.7% |
|  Appanoose |                    0.0 |                             0.0 |               \-36.3% |
