Compiled at 2021-04-11 17:11:20 UTC

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

## Tables as of 2021-04-11

As of 2021-04-11, IPDH is reporting 432 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   88.9 |                            18.1 |               \-20.6% |
|          Linn |                   25.6 |                            11.3 |                  8.1% |
|         Scott |                   57.6 |                            33.3 |                \-5.3% |
|       Johnson |                   28.7 |                            19.0 |                  5.0% |
|    Black Hawk |                   17.1 |                            13.1 |                  5.0% |
|      Woodbury |                   21.7 |                            21.1 |               \-29.0% |
|       Dubuque |                   27.9 |                            28.6 |                 18.8% |
|         Story |                   14.4 |                            14.9 |               \-40.0% |
|        Dallas |                   13.6 |                            14.5 |               \-30.6% |
| Pottawattamie |                   24.6 |                            26.4 |               \-17.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.0 |                            52.1 |               \-24.7% |
|   Osceola |                    2.3 |                            38.4 |                 27.8% |
|      Clay |                    6.1 |                            38.4 |               \-13.8% |
|  Delaware |                    5.7 |                            33.6 |                  0.0% |
|     Scott |                   57.6 |                            33.3 |                \-5.3% |
|     Emmet |                    3.0 |                            32.6 |               \-31.7% |
|     Worth |                    2.3 |                            31.0 |                 77.0% |
|  Plymouth |                    7.4 |                            29.5 |               \-19.2% |
|    Shelby |                    3.3 |                            28.7 |                 66.7% |
|   Dubuque |                   27.9 |                            28.6 |                 18.8% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                    5.1 |                            25.5 |                126.3% |
|     Mahaska |                    4.3 |                            19.4 |                117.6% |
|      Taylor |                    0.9 |                            14.0 |                 85.7% |
|       Worth |                    2.3 |                            31.0 |                 77.0% |
|      Shelby |                    3.3 |                            28.7 |                 66.7% |
|     Clayton |                    3.0 |                            17.1 |                 55.6% |
|        Page |                    3.9 |                            25.5 |                 54.5% |
|  Montgomery |                    1.7 |                            17.3 |                 46.1% |
| Cerro Gordo |                    8.6 |                            20.2 |                 45.7% |
|  Washington |                    3.7 |                            16.9 |                 43.5% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Guthrie |                    0.9 |                             8.0 |               \-59.4% |
|     Monona |                    0.6 |                             6.6 |               \-42.1% |
|      Story |                   14.4 |                            14.9 |               \-40.0% |
|     Clarke |                    0.3 |                             3.0 |               \-40.0% |
|      Cedar |                    2.4 |                            13.0 |               \-38.4% |
|   Buchanan |                    2.0 |                             9.4 |               \-38.2% |
|     Jasper |                    2.9 |                             7.7 |               \-37.2% |
| Pocahontas |                    0.0 |                             0.0 |               \-36.3% |
|  Appanoose |                    0.3 |                             2.3 |               \-35.7% |
|     Benton |                    1.0 |                             3.9 |               \-33.3% |
