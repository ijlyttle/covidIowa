Compiled at 2021-04-14 00:02:42 UTC

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

## Tables as of 2021-04-13

As of 2021-04-13, IPDH is reporting 445 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   91.7 |                            18.7 |                \-9.6% |
|          Linn |                   25.6 |                            11.3 |                  4.5% |
|         Scott |                   60.0 |                            34.7 |                \-4.9% |
|       Johnson |                   28.4 |                            18.8 |                \-6.8% |
|    Black Hawk |                   17.1 |                            13.1 |                 15.5% |
|      Woodbury |                   19.6 |                            19.0 |               \-32.7% |
|       Dubuque |                   25.7 |                            26.4 |                \-5.6% |
|         Story |                   13.9 |                            14.3 |               \-43.2% |
|        Dallas |                   13.7 |                            14.7 |               \-16.3% |
| Pottawattamie |                   24.4 |                            26.2 |               \-18.3% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    8.0 |                            46.4 |               \-34.4% |
|   Osceola |                    2.3 |                            38.4 |                  9.5% |
|      Clay |                    5.6 |                            34.8 |               \-28.1% |
|     Scott |                   60.0 |                            34.7 |                \-4.9% |
|     Emmet |                    3.0 |                            32.6 |               \-30.0% |
|    Shelby |                    3.4 |                            29.9 |                 72.3% |
|   Fremont |                    2.0 |                            28.7 |                  5.0% |
|     Worth |                    2.0 |                            27.1 |                 31.2% |
|  Delaware |                    4.6 |                            26.9 |               \-29.1% |
|   Dubuque |                   25.7 |                            26.4 |                \-5.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Taylor |                    1.0 |                            16.3 |                100.0% |
|     Shelby |                    3.4 |                            29.9 |                 72.3% |
|      Mills |                    2.9 |                            18.9 |                 50.0% |
|     Wright |                    2.4 |                            19.3 |                 50.0% |
|    Mahaska |                    3.9 |                            17.5 |                 47.8% |
| Washington |                    3.9 |                            17.6 |                 36.0% |
| Montgomery |                    1.7 |                            17.3 |                 35.7% |
|     Monroe |                    1.7 |                            22.2 |                 35.7% |
| Des Moines |                    4.1 |                            10.6 |                 33.3% |
|      Adams |                    0.7 |                            19.8 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Guthrie |                    0.9 |                             8.0 |               \-58.1% |
|  Carroll |                    1.9 |                             9.2 |               \-57.4% |
| Plymouth |                    5.4 |                            21.6 |               \-51.1% |
|    Cedar |                    2.1 |                            11.5 |               \-46.3% |
|   Monona |                    0.4 |                             5.0 |               \-44.4% |
|    Story |                   13.9 |                            14.3 |               \-43.2% |
|   Benton |                    1.0 |                             3.9 |               \-39.1% |
| Marshall |                    1.7 |                             4.4 |               \-38.7% |
|     Page |                    2.4 |                            16.1 |               \-38.4% |
|  Jackson |                    1.7 |                             8.8 |               \-36.7% |
