Compiled at 2021-04-17 00:00:03 UTC

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

As of 2021-04-16, IPDH is reporting 583 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |
| 2021-04-10 |                  521.3 |                            16.5 |               \-13.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   84.3 |                            17.2 |                \-0.8% |
|          Linn |                   26.6 |                            11.7 |                 25.3% |
|         Scott |                   62.3 |                            36.0 |                 10.5% |
|       Johnson |                   31.6 |                            20.9 |                  9.6% |
|    Black Hawk |                   15.0 |                            11.4 |                \-9.7% |
|      Woodbury |                   21.9 |                            21.2 |                  2.6% |
|       Dubuque |                   21.0 |                            21.6 |               \-24.1% |
|         Story |                   11.4 |                            11.8 |               \-24.3% |
|        Dallas |                   13.0 |                            13.9 |                  5.4% |
| Pottawattamie |                   22.7 |                            24.4 |               \-13.1% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    2.7 |                            45.6 |                 36.8% |
|         Scott |                   62.3 |                            36.0 |                 10.5% |
|     Dickinson |                    5.4 |                            31.5 |               \-45.8% |
|           Ida |                    1.9 |                            27.1 |                 81.9% |
|         Worth |                    1.9 |                            25.2 |                  5.3% |
|          Clay |                    4.0 |                            25.0 |               \-27.1% |
| Pottawattamie |                   22.7 |                            24.4 |               \-13.1% |
|           Sac |                    2.3 |                            23.5 |                 27.8% |
|        Warren |                   12.0 |                            23.3 |                 35.8% |
|         Emmet |                    2.1 |                            23.3 |               \-37.1% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Hamilton |                    2.0 |                            13.5 |                109.9% |
|        Ida |                    1.9 |                            27.1 |                 81.9% |
|    Guthrie |                    1.9 |                            17.4 |                 66.7% |
| Pocahontas |                    0.6 |                             8.6 |                 57.1% |
|     Hardin |                    2.7 |                            16.1 |                 36.8% |
|    Madison |                    2.7 |                            16.6 |                 36.8% |
|    Osceola |                    2.7 |                            45.6 |                 36.8% |
|     Warren |                   12.0 |                            23.3 |                 35.8% |
|      Adair |                    0.7 |                            10.0 |                 33.3% |
|     Grundy |                    0.9 |                             7.0 |                 30.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Carroll |                    1.9 |                             9.2 |               \-55.6% |
|     Davis |                    0.1 |                             1.6 |               \-55.5% |
|     Union |                    0.4 |                             3.5 |               \-50.0% |
| Dickinson |                    5.4 |                            31.5 |               \-45.8% |
|    Marion |                    1.6 |                             4.7 |               \-37.9% |
|   Kossuth |                    2.3 |                            15.4 |               \-37.8% |
|     Emmet |                    2.1 |                            23.3 |               \-37.1% |
|  Mitchell |                    0.0 |                             0.0 |               \-36.3% |
|  Harrison |                    2.3 |                            16.3 |               \-36.1% |
|  Franklin |                    0.3 |                             2.8 |               \-35.7% |
