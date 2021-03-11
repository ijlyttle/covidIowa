Compiled at 2021-03-11 17:59:02 UTC

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

## Tables as of 2021-03-11

As of 2021-03-11, IPDH is reporting 412 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  113.4 |                            23.1 |                 19.7% |
|          Linn |                   15.6 |                             6.9 |               \-21.6% |
|         Scott |                   29.6 |                            17.1 |                 56.2% |
|       Johnson |                   14.1 |                             9.4 |               \-18.5% |
|    Black Hawk |                   17.6 |                            13.4 |                 35.4% |
|      Woodbury |                   27.1 |                            26.3 |                 41.7% |
|       Dubuque |                   10.9 |                            11.2 |               \-29.1% |
|         Story |                   19.7 |                            20.3 |                  7.4% |
|        Dallas |                   19.7 |                            21.1 |               \-14.2% |
| Pottawattamie |                   16.6 |                            17.8 |                 14.9% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.3 |                            62.5 |                164.3% |
|     Wayne |                    4.0 |                            62.1 |                249.9% |
|   Madison |                    6.9 |                            42.0 |                129.1% |
|      Clay |                    6.6 |                            41.0 |                253.3% |
| Dickinson |                    6.6 |                            38.1 |                 96.3% |
|      Page |                    5.6 |                            36.9 |                 70.4% |
| Allamakee |                    5.0 |                            36.5 |                 13.5% |
|  Cherokee |                    3.9 |                            34.3 |                 79.0% |
|    Shelby |                    3.7 |                            32.4 |                 32.0% |
|       Sac |                    3.0 |                            30.9 |                 47.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|        Clay |                    6.6 |                            41.0 |                253.3% |
|       Wayne |                    4.0 |                            62.1 |                249.9% |
|         Ida |                    4.3 |                            62.5 |                164.3% |
|     Madison |                    6.9 |                            42.0 |                129.1% |
|    Delaware |                    2.6 |                            15.1 |                108.3% |
|       Floyd |                    2.7 |                            17.4 |                100.0% |
|   Dickinson |                    6.6 |                            38.1 |                 96.3% |
| Cerro Gordo |                    6.6 |                            15.5 |                 89.3% |
|    Cherokee |                    3.9 |                            34.3 |                 79.0% |
|    Franklin |                    1.3 |                            12.8 |                 77.8% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Fremont |                  \-0.1 |                           \-2.1 |               \-62.5% |
|         Lee |                    1.3 |                             3.8 |               \-56.8% |
|      Jasper |                    6.9 |                            18.4 |               \-56.7% |
|      Taylor |                  \-0.3 |                           \-4.7 |               \-54.6% |
|   Jefferson |                    0.6 |                             3.1 |               \-50.0% |
| Buena Vista |                    2.7 |                            13.8 |               \-46.9% |
|       Worth |                    0.6 |                             7.7 |               \-42.1% |
|    Hamilton |                    0.4 |                             2.9 |               \-41.2% |
|     Osceola |                    0.4 |                             7.2 |               \-37.5% |
|        Cass |                    2.6 |                            20.0 |               \-34.2% |
