Compiled at 2021-04-04 00:05:36 UTC

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

## Tables as of 2021-04-03

As of 2021-04-03, IPDH is reporting 551 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  114.0 |                            23.3 |                  9.8% |
|          Linn |                   21.7 |                             9.6 |                 31.4% |
|         Scott |                   62.0 |                            35.9 |                 18.2% |
|       Johnson |                   27.1 |                            18.0 |                 27.1% |
|    Black Hawk |                   16.7 |                            12.7 |                 37.8% |
|      Woodbury |                   31.4 |                            30.5 |                 19.5% |
|       Dubuque |                   23.3 |                            23.9 |                 54.6% |
|         Story |                   26.0 |                            26.8 |                 39.0% |
|        Dallas |                   20.9 |                            22.3 |                  7.0% |
| Pottawattamie |                   29.9 |                            32.0 |                 41.2% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   14.1 |                            82.0 |                 23.3% |
|         Emmet |                    5.7 |                            62.1 |                 38.2% |
|          Clay |                    7.3 |                            45.5 |               \-22.7% |
|     Palo Alto |                    3.6 |                            40.2 |                 33.3% |
|      Plymouth |                    9.3 |                            36.9 |                 24.1% |
|       Guthrie |                    3.9 |                            36.1 |                 21.4% |
|         Scott |                   62.0 |                            35.9 |                 18.2% |
|      Delaware |                    5.7 |                            33.6 |                 14.6% |
|       Osceola |                    2.0 |                            33.6 |               \-12.5% |
| Pottawattamie |                   29.9 |                            32.0 |                 41.2% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Cedar |                    4.9 |                            26.1 |                105.0% |
|    Benton |                    3.3 |                            12.8 |                100.0% |
|     Union |                    2.0 |                            16.3 |                 75.0% |
|     Henry |                    2.7 |                            13.6 |                 73.3% |
|     Jones |                    2.7 |                            13.1 |                 62.5% |
| Chickasaw |                    0.9 |                             7.2 |                 62.5% |
|    Clarke |                    1.3 |                            13.7 |                 60.0% |
|   Dubuque |                   23.3 |                            23.9 |                 54.6% |
| Appanoose |                    1.4 |                            11.5 |                 54.6% |
|     Floyd |                    2.3 |                            14.6 |                 53.3% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Lee |                    2.4 |                             7.2 |               \-72.1% |
|  Wapello |                    3.4 |                             9.8 |               \-45.6% |
|   Jasper |                    5.6 |                            15.0 |               \-41.8% |
|    Wayne |                    0.7 |                            11.1 |               \-36.8% |
|     Tama |                    0.4 |                             2.5 |               \-33.3% |
|   Shelby |                    2.1 |                            18.7 |               \-33.3% |
| Humboldt |                    1.0 |                            10.5 |               \-33.3% |
|   Greene |                    0.4 |                             4.8 |               \-33.3% |
|   Howard |                    0.4 |                             4.7 |               \-28.6% |
| Ringgold |                    0.6 |                            11.7 |               \-26.7% |
