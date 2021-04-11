Compiled at 2021-04-11 00:00:38 UTC

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

## Tables as of 2021-04-10

As of 2021-04-10, IPDH is reporting 616 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   88.7 |                            18.1 |               \-22.0% |
|          Linn |                   24.3 |                            10.7 |                 11.3% |
|         Scott |                   58.4 |                            33.8 |                \-5.7% |
|       Johnson |                   27.3 |                            18.1 |                  0.5% |
|    Black Hawk |                   17.0 |                            13.0 |                  1.6% |
|      Woodbury |                   21.7 |                            21.1 |               \-30.0% |
|       Dubuque |                   27.4 |                            28.2 |                 17.1% |
|         Story |                   14.6 |                            15.0 |               \-42.3% |
|        Dallas |                   13.7 |                            14.7 |               \-32.7% |
| Pottawattamie |                   24.7 |                            26.5 |               \-16.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.1 |                            53.0 |               \-33.0% |
|     Emmet |                    3.4 |                            37.2 |               \-34.0% |
|   Osceola |                    2.1 |                            36.0 |                  4.8% |
|      Clay |                    5.6 |                            34.8 |               \-20.7% |
|  Delaware |                    5.9 |                            34.4 |                  2.1% |
|     Scott |                   58.4 |                            33.8 |                \-5.7% |
|    Shelby |                    3.6 |                            31.2 |                 45.4% |
|  Plymouth |                    7.7 |                            30.6 |               \-15.3% |
|   Dubuque |                   27.4 |                            28.2 |                 17.1% |
|   Fremont |                    1.9 |                            26.7 |                 11.1% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Mahaska |                    3.7 |                            16.8 |                 83.4% |
|  Clayton |                    3.1 |                            17.9 |                 81.2% |
|   Taylor |                    0.7 |                            11.7 |                 71.4% |
|  Carroll |                    4.6 |                            22.7 |                 69.5% |
|    Worth |                    1.9 |                            25.2 |                 53.9% |
| Harrison |                    3.6 |                            25.4 |                 52.4% |
|     Page |                    4.0 |                            26.5 |                 52.2% |
|     Tama |                    1.1 |                             6.8 |                 50.0% |
|   Wright |                    2.0 |                            15.9 |                 50.0% |
|   Shelby |                    3.6 |                            31.2 |                 45.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Guthrie |                    1.0 |                             9.4 |               \-58.8% |
|     Benton |                    1.0 |                             3.9 |               \-53.3% |
|     Clarke |                    0.1 |                             1.5 |               \-50.0% |
|  Appanoose |                    0.3 |                             2.3 |               \-47.1% |
|   Humboldt |                    0.1 |                             1.5 |               \-42.8% |
|      Story |                   14.6 |                            15.0 |               \-42.3% |
|   Mitchell |                    0.6 |                             5.4 |               \-42.1% |
|     Monona |                    0.6 |                             6.6 |               \-42.1% |
| Pocahontas |                    0.0 |                             0.0 |               \-41.7% |
|  Van Buren |                    0.3 |                             4.1 |               \-40.0% |
