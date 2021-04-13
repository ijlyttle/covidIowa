Compiled at 2021-04-13 00:02:08 UTC

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

## Tables as of 2021-04-12

As of 2021-04-12, IPDH is reporting 146 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   89.9 |                            18.3 |                \-1.4% |
|          Linn |                   26.9 |                            11.8 |                 25.0% |
|         Scott |                   58.9 |                            34.0 |                  2.2% |
|       Johnson |                   28.6 |                            18.9 |                  6.7% |
|    Black Hawk |                   17.7 |                            13.5 |                 33.7% |
|      Woodbury |                   21.0 |                            20.4 |               \-21.4% |
|       Dubuque |                   27.4 |                            28.2 |                 17.8% |
|         Story |                   14.0 |                            14.4 |               \-37.5% |
|        Dallas |                   13.4 |                            14.4 |                \-6.5% |
| Pottawattamie |                   24.3 |                            26.1 |               \-13.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    8.9 |                            51.3 |               \-21.6% |
|   Osceola |                    2.4 |                            40.8 |                 50.0% |
|      Clay |                    6.3 |                            39.2 |                \-1.9% |
|     Emmet |                    3.1 |                            34.1 |               \-21.6% |
|     Scott |                   58.9 |                            34.0 |                  2.2% |
|  Delaware |                    5.3 |                            31.1 |                \-8.3% |
|     Worth |                    2.3 |                            31.0 |                 64.3% |
|    Shelby |                    3.3 |                            28.7 |                 76.5% |
|   Dubuque |                   27.4 |                            28.2 |                 17.8% |
|  Plymouth |                    6.9 |                            27.2 |               \-25.7% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Mahaska |                    4.1 |                            18.8 |                125.0% |
|    Carroll |                    5.1 |                            25.5 |                115.0% |
|     Taylor |                    1.0 |                            16.3 |                100.0% |
|    Clayton |                    3.1 |                            17.9 |                 93.3% |
| Washington |                    4.0 |                            18.2 |                 84.2% |
|     Shelby |                    3.3 |                            28.7 |                 76.5% |
|      Worth |                    2.3 |                            31.0 |                 64.3% |
|      Mills |                    2.6 |                            17.0 |                 56.2% |
|       Page |                    3.9 |                            25.5 |                 54.5% |
|    Osceola |                    2.4 |                            40.8 |                 50.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Monona |                    0.1 |                             1.7 |               \-57.9% |
|   Guthrie |                    0.9 |                             8.0 |               \-55.2% |
| Appanoose |                    0.1 |                             1.2 |               \-42.8% |
|   Audubon |                    0.3 |                             5.2 |               \-40.0% |
|    Benton |                    0.9 |                             3.3 |               \-38.1% |
|     Story |                   14.0 |                            14.4 |               \-37.5% |
|  Buchanan |                    1.9 |                             8.8 |               \-37.5% |
|    Clarke |                    0.3 |                             3.0 |               \-35.7% |
| Van Buren |                    0.3 |                             4.1 |               \-35.7% |
|       Sac |                    1.3 |                            13.2 |               \-33.3% |
