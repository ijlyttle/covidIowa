Compiled at 2021-04-01 17:18:33 UTC

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

## Tables as of 2021-04-01

As of 2021-04-01, IPDH is reporting 810 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  126.0 |                            25.7 |                  9.8% |
|          Linn |                   22.6 |                            10.0 |                 13.8% |
|         Scott |                   69.9 |                            40.4 |                 84.4% |
|       Johnson |                   27.1 |                            18.0 |                 48.1% |
|    Black Hawk |                   16.1 |                            12.3 |                 17.7% |
|      Woodbury |                   32.1 |                            31.2 |                \-5.3% |
|       Dubuque |                   22.3 |                            22.9 |                 75.3% |
|         Story |                   27.4 |                            28.2 |                 61.8% |
|        Dallas |                   25.3 |                            27.1 |                 31.4% |
| Pottawattamie |                   26.1 |                            28.0 |                 19.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   13.7 |                            79.5 |                 21.2% |
|      Clay |                   10.1 |                            63.3 |                 18.2% |
|     Emmet |                    5.6 |                            60.5 |                 35.3% |
| Palo Alto |                    5.1 |                            57.9 |                126.3% |
|   Guthrie |                    5.0 |                            46.8 |                 68.0% |
|   Osceola |                    2.7 |                            45.6 |                 36.8% |
|     Scott |                   69.9 |                            40.4 |                 84.4% |
|  Delaware |                    6.6 |                            38.6 |                 55.9% |
|  Plymouth |                    9.3 |                            36.9 |                 22.0% |
|       Lee |                   12.0 |                            35.7 |                600.1% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                   12.0 |                            35.7 |                600.1% |
|   Palo Alto |                    5.1 |                            57.9 |                126.3% |
|       Cedar |                    3.9 |                            20.7 |                112.5% |
|      Shelby |                    4.0 |                            34.9 |                 94.5% |
|       Scott |                   69.9 |                            40.4 |                 84.4% |
|      Jasper |                   10.9 |                            29.2 |                 80.4% |
|      Clarke |                    1.3 |                            13.7 |                 77.8% |
|     Dubuque |                   22.3 |                            22.9 |                 75.3% |
| Cerro Gordo |                    6.7 |                            15.8 |                 74.2% |
|     Guthrie |                    5.0 |                            46.8 |                 68.0% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|    Lucas |                    0.1 |                             1.7 |               \-52.9% |
|     Tama |                    0.3 |                             1.7 |               \-52.6% |
|  Wapello |                    3.9 |                            11.0 |               \-51.4% |
|    Wayne |                    0.9 |                            13.3 |               \-50.0% |
|    Worth |                    0.3 |                             3.9 |               \-40.0% |
| Harrison |                    1.0 |                             7.1 |               \-39.1% |
|   Howard |                    0.6 |                             6.2 |               \-38.9% |
|    Adair |                    0.4 |                             6.0 |               \-37.5% |
|      Ida |                    1.1 |                            16.7 |               \-37.5% |
| Humboldt |                    1.4 |                            15.0 |               \-32.0% |
