Compiled at 2021-03-19 17:08:31 UTC

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

## Tables as of 2021-03-19

As of 2021-03-19, IPDH is reporting 595 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   96.4 |                            19.7 |               \-10.8% |
|          Linn |                   16.3 |                             7.2 |                 17.5% |
|         Scott |                   22.4 |                            13.0 |               \-19.2% |
|       Johnson |                   10.6 |                             7.0 |               \-17.4% |
|    Black Hawk |                   12.1 |                             9.3 |               \-22.7% |
|      Woodbury |                   32.6 |                            31.6 |                 19.9% |
|       Dubuque |                    8.0 |                             8.2 |               \-14.9% |
|         Story |                   12.3 |                            12.7 |               \-32.1% |
|        Dallas |                   14.7 |                            15.7 |               \-21.4% |
| Pottawattamie |                   14.6 |                            15.6 |               \-16.8% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    8.1 |                            47.2 |                  3.2% |
|  Cherokee |                    3.9 |                            34.3 |                \-5.6% |
|     Emmet |                    3.0 |                            32.6 |                 64.7% |
|   O’Brien |                    4.4 |                            32.2 |                 26.7% |
|  Woodbury |                   32.6 |                            31.6 |                 19.9% |
|      Clay |                    5.0 |                            31.2 |               \-22.2% |
|       Ida |                    2.0 |                            29.2 |               \-47.5% |
|     Wayne |                    1.9 |                            28.8 |               \-41.2% |
|   Kossuth |                    4.0 |                            27.0 |                 59.1% |
|  Plymouth |                    6.1 |                            24.4 |                \-3.8% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Pocahontas |                    1.4 |                            21.6 |                 88.9% |
|      Emmet |                    3.0 |                            32.6 |                 64.7% |
|    Clayton |                    1.6 |                             9.0 |                 63.7% |
|    Fremont |                    0.9 |                            12.3 |                 62.5% |
|    Kossuth |                    4.0 |                            27.0 |                 59.1% |
|   Hamilton |                    1.4 |                             9.7 |                 54.6% |
|  Appanoose |                    1.1 |                             9.2 |                 50.0% |
| Montgomery |                    0.6 |                             5.8 |                 37.4% |
|      Sioux |                    6.4 |                            18.4 |                 26.8% |
|    O’Brien |                    4.4 |                            32.2 |                 26.7% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|        Page |                    1.4 |                             9.5 |               \-62.2% |
|     Madison |                    2.0 |                            12.2 |               \-61.8% |
|   Allamakee |                    1.6 |                            11.5 |               \-59.1% |
|      Jasper |                    2.3 |                             6.1 |               \-57.4% |
|      Marion |                    2.9 |                             8.6 |               \-53.5% |
| Cerro Gordo |                    2.9 |                             6.7 |               \-49.1% |
|      Benton |                    2.0 |                             7.8 |               \-48.8% |
|         Ida |                    2.0 |                            29.2 |               \-47.5% |
|       Cedar |                    2.0 |                            10.7 |               \-43.2% |
|      Grundy |                    0.1 |                             1.2 |               \-42.8% |
