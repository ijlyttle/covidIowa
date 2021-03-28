Compiled at 2021-03-28 20:19:41 UTC

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

## Tables as of 2021-03-28

As of 2021-03-28, IPDH is reporting 458 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-28 |                  560.3 |                            17.8 |                 33.6% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  115.0 |                            23.5 |                 19.9% |
|          Linn |                   16.7 |                             7.4 |                  6.0% |
|         Scott |                   56.6 |                            32.7 |                129.0% |
|       Johnson |                   21.7 |                            14.4 |                 69.1% |
|    Black Hawk |                   13.4 |                            10.2 |                 32.9% |
|      Woodbury |                   27.0 |                            26.2 |                \-4.9% |
|       Dubuque |                   16.3 |                            16.7 |                101.7% |
|         Story |                   19.9 |                            20.4 |                 46.0% |
|        Dallas |                   22.1 |                            23.7 |                 51.4% |
| Pottawattamie |                   21.4 |                            23.0 |                 30.8% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.6 |                            67.0 |                 18.9% |
|     Emmet |                    5.3 |                            57.4 |                 76.0% |
|      Clay |                    9.0 |                            56.2 |                 59.1% |
|   Osceola |                    2.9 |                            48.0 |                125.0% |
|    Shelby |                    4.0 |                            34.9 |                105.8% |
|   Guthrie |                    3.7 |                            34.7 |                135.7% |
|       Lee |                   11.4 |                            34.0 |                769.8% |
|     Scott |                   56.6 |                            32.7 |                129.0% |
| Palo Alto |                    2.9 |                            32.2 |                 42.1% |
|  Cherokee |                    3.6 |                            31.8 |                 39.1% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                   11.4 |                            34.0 |                769.8% |
|      Jasper |                   10.6 |                            28.4 |                189.3% |
|     Guthrie |                    3.7 |                            34.7 |                135.7% |
|       Scott |                   56.6 |                            32.7 |                129.0% |
|     Osceola |                    2.9 |                            48.0 |                125.0% |
|      Shelby |                    4.0 |                            34.9 |                105.8% |
|     Dubuque |                   16.3 |                            16.7 |                101.7% |
|       Emmet |                    5.3 |                            57.4 |                 76.0% |
|  Washington |                    3.0 |                            13.7 |                 75.0% |
| Cerro Gordo |                    4.7 |                            11.1 |                 73.9% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Poweshiek |                    0.0 |                             0.0 |               \-61.1% |
|   Wapello |                    3.4 |                             9.8 |               \-53.7% |
|     Adair |                    0.3 |                             4.0 |               \-47.1% |
|  Crawford |                    1.0 |                             5.9 |               \-44.0% |
|     Lucas |                    0.3 |                             3.3 |               \-43.7% |
|    Monroe |                    0.1 |                             1.9 |               \-42.8% |
| Chickasaw |                    0.1 |                             1.2 |               \-38.4% |
| Appanoose |                    0.4 |                             3.5 |               \-37.5% |
|   Calhoun |                    0.7 |                             7.4 |               \-36.8% |
|    Louisa |                    0.4 |                             3.9 |               \-33.3% |
