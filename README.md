Compiled at 2021-04-15 20:19:08 UTC

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

## Tables as of 2021-04-15

As of 2021-04-15, IPDH is reporting 538 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   79.7 |                            16.3 |               \-10.7% |
|          Linn |                   25.1 |                            11.1 |                 24.5% |
|         Scott |                   56.9 |                            32.9 |                \-5.4% |
|       Johnson |                   28.3 |                            18.7 |                \-0.5% |
|    Black Hawk |                   15.0 |                            11.4 |                \-3.4% |
|      Woodbury |                   22.3 |                            21.6 |                  0.6% |
|       Dubuque |                   21.9 |                            22.5 |               \-22.3% |
|         Story |                   11.9 |                            12.2 |               \-31.3% |
|        Dallas |                   13.3 |                            14.2 |                  3.1% |
| Pottawattamie |                   24.0 |                            25.7 |               \-11.6% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    3.1 |                            52.8 |                 61.1% |
|         Emmet |                    3.3 |                            35.7 |                \-9.1% |
|     Dickinson |                    5.9 |                            33.9 |               \-44.8% |
|         Scott |                   56.9 |                            32.9 |                \-5.4% |
|           Ida |                    2.1 |                            31.2 |                 83.4% |
|       Fremont |                    1.9 |                            26.7 |                 25.0% |
|        Shelby |                    3.0 |                            26.2 |                 64.7% |
| Pottawattamie |                   24.0 |                            25.7 |               \-11.6% |
|      Plymouth |                    6.3 |                            25.0 |               \-30.1% |
|      Delaware |                    4.1 |                            24.4 |               \-16.3% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    2.1 |                            31.2 |                 83.4% |
|    Taylor |                    1.0 |                            16.3 |                 75.0% |
|    Shelby |                    3.0 |                            26.2 |                 64.7% |
|     Adams |                    0.9 |                            23.8 |                 62.5% |
|   Osceola |                    3.1 |                            52.8 |                 61.1% |
|    Butler |                    1.3 |                             8.9 |                 60.0% |
|  Hamilton |                    1.9 |                            12.6 |                 53.9% |
|    Wright |                    2.6 |                            20.5 |                 47.0% |
| Appanoose |                    1.3 |                            10.3 |                 45.5% |
|   Wapello |                    2.4 |                             6.9 |                 33.4% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Davis |                    0.1 |                             1.6 |               \-55.5% |
|   Carroll |                    2.3 |                            11.3 |               \-51.1% |
| Jefferson |                  \-0.1 |                           \-0.8 |               \-50.0% |
|     Cedar |                    1.7 |                             9.2 |               \-48.7% |
| Dickinson |                    5.9 |                            33.9 |               \-44.8% |
|   Clayton |                    1.6 |                             9.0 |               \-43.8% |
|    Greene |                    0.3 |                             3.2 |               \-43.7% |
|   Calhoun |                    0.0 |                             0.0 |               \-41.7% |
|    Bremer |                    1.0 |                             4.0 |               \-39.1% |
|  Marshall |                    1.3 |                             3.3 |               \-38.4% |
