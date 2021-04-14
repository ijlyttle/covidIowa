Compiled at 2021-04-14 17:09:24 UTC

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

## Tables as of 2021-04-14

As of 2021-04-14, IPDH is reporting 655 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   88.6 |                            18.1 |                \-4.6% |
|          Linn |                   24.0 |                            10.6 |                  3.5% |
|         Scott |                   56.7 |                            32.8 |               \-10.8% |
|       Johnson |                   29.6 |                            19.6 |                  9.7% |
|    Black Hawk |                   15.7 |                            12.0 |                  6.4% |
|      Woodbury |                   22.0 |                            21.3 |                \-3.0% |
|       Dubuque |                   24.0 |                            24.7 |               \-17.5% |
|         Story |                   12.3 |                            12.7 |               \-33.1% |
|        Dallas |                   12.9 |                            13.8 |                \-5.8% |
| Pottawattamie |                   23.6 |                            25.3 |               \-17.3% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    3.0 |                            50.4 |                 55.6% |
|     Dickinson |                    7.3 |                            42.2 |               \-42.6% |
|         Emmet |                    3.3 |                            35.7 |               \-23.1% |
|       Fremont |                    2.3 |                            32.8 |                 21.1% |
|         Scott |                   56.7 |                            32.8 |               \-10.8% |
|      Delaware |                    4.9 |                            28.6 |               \-10.9% |
|           Ida |                    1.9 |                            27.1 |                 66.7% |
|      Harrison |                    3.7 |                            26.4 |                 26.9% |
| Pottawattamie |                   23.6 |                            25.3 |               \-17.3% |
|          Clay |                    4.0 |                            25.0 |               \-39.7% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Mills |                    2.9 |                            18.9 |                 80.0% |
|     Wright |                    2.3 |                            18.2 |                 77.0% |
|     Taylor |                    1.0 |                            16.3 |                 75.0% |
|        Ida |                    1.9 |                            27.1 |                 66.7% |
|     Shelby |                    2.6 |                            22.4 |                 66.6% |
|    Osceola |                    3.0 |                            50.4 |                 55.6% |
|    Clayton |                    3.3 |                            18.7 |                 42.9% |
|   Hamilton |                    1.4 |                             9.7 |                 41.7% |
|  Chickasaw |                    1.1 |                             9.6 |                 36.4% |
| Montgomery |                    1.9 |                            18.7 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Monona |                    0.1 |                             1.7 |               \-57.9% |
|   Carroll |                    2.1 |                            10.6 |               \-50.0% |
|     Cedar |                    1.9 |                            10.0 |               \-42.9% |
| Dickinson |                    7.3 |                            42.2 |               \-42.6% |
| Jefferson |                    0.0 |                             0.0 |               \-41.7% |
|  Crawford |                    1.0 |                             5.9 |               \-41.7% |
|       Sac |                    1.4 |                            14.7 |               \-41.4% |
|      Clay |                    4.0 |                            25.0 |               \-39.7% |
| Palo Alto |                    1.4 |                            16.1 |               \-39.3% |
|  Plymouth |                    6.0 |                            23.8 |               \-38.8% |
