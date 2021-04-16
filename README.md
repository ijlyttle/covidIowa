Compiled at 2021-04-16 17:13:32 UTC

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

## Tables as of 2021-04-16

As of 2021-04-16, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-16 |                  404.6 |                            12.8 |               \-20.9% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   68.1 |                            13.9 |               \-19.6% |
|          Linn |                   21.9 |                             9.6 |                  3.9% |
|         Scott |                   48.4 |                            28.0 |               \-13.7% |
|       Johnson |                   25.1 |                            16.6 |               \-12.0% |
|    Black Hawk |                   12.0 |                             9.1 |               \-26.6% |
|      Woodbury |                   20.0 |                            19.4 |                \-5.8% |
|       Dubuque |                   18.4 |                            18.9 |               \-33.0% |
|         Story |                    9.7 |                            10.0 |               \-34.8% |
|        Dallas |                   11.7 |                            12.5 |                \-4.3% |
| Pottawattamie |                   20.0 |                            21.5 |               \-23.0% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    2.6 |                            43.2 |                 31.6% |
|         Scott |                   48.4 |                            28.0 |               \-13.7% |
|           Ida |                    1.9 |                            27.1 |                 81.9% |
|     Dickinson |                    4.6 |                            26.5 |               \-53.0% |
|       Fremont |                    1.6 |                            22.6 |                  0.0% |
|         Emmet |                    2.0 |                            21.7 |               \-40.0% |
| Pottawattamie |                   20.0 |                            21.5 |               \-23.0% |
|         Worth |                    1.6 |                            21.3 |                \-5.3% |
|          Page |                    3.0 |                            19.9 |                  3.7% |
|       Clinton |                    9.1 |                            19.7 |                \-5.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Hamilton |                    1.9 |                            12.6 |                 99.9% |
|        Ida |                    1.9 |                            27.1 |                 81.9% |
|  Appanoose |                    1.1 |                             9.2 |                 36.4% |
|    Audubon |                    0.7 |                            13.0 |                 33.3% |
|    Osceola |                    2.6 |                            43.2 |                 31.6% |
|     Grundy |                    0.9 |                             7.0 |                 30.0% |
| Pocahontas |                    0.3 |                             4.3 |                 28.6% |
|     Hardin |                    2.4 |                            14.4 |                 26.3% |
|    Guthrie |                    1.1 |                            10.7 |                 25.0% |
| Des Moines |                    3.6 |                             9.2 |                 23.1% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Crawford |                    0.1 |                             0.8 |               \-63.6% |
|     Davis |                    0.1 |                             1.6 |               \-55.5% |
|   Carroll |                    2.0 |                             9.9 |               \-53.3% |
| Dickinson |                    4.6 |                            26.5 |               \-53.0% |
|     Union |                    0.4 |                             3.5 |               \-50.0% |
|  Harrison |                    1.9 |                            13.2 |               \-44.4% |
|      Clay |                    2.9 |                            17.8 |               \-43.8% |
|   Kossuth |                    2.0 |                            13.5 |               \-43.2% |
|    Marion |                    1.4 |                             4.3 |               \-41.4% |
| Jefferson |                  \-0.1 |                           \-0.8 |               \-40.0% |
