Compiled at 2021-03-30 20:20:42 UTC

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

## Tables as of 2021-03-30

As of 2021-03-30, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  114.4 |                            23.3 |                 25.1% |
|          Linn |                   15.0 |                             6.6 |                \-5.9% |
|         Scott |                   56.3 |                            32.5 |                121.5% |
|       Johnson |                   20.6 |                            13.6 |                 48.0% |
|    Black Hawk |                   14.3 |                            10.9 |                 42.7% |
|      Woodbury |                   27.6 |                            26.7 |                  0.5% |
|       Dubuque |                   16.4 |                            16.9 |                 93.7% |
|         Story |                   19.9 |                            20.4 |                 46.0% |
|        Dallas |                   23.3 |                            24.9 |                 61.9% |
| Pottawattamie |                   21.7 |                            23.3 |                 30.3% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.7 |                            67.9 |                 20.3% |
|     Emmet |                    5.3 |                            57.4 |                 83.3% |
|      Clay |                    8.9 |                            55.3 |                 50.0% |
|   Osceola |                    3.0 |                            50.4 |                133.4% |
|    Shelby |                    4.0 |                            34.9 |                105.8% |
|   Guthrie |                    3.7 |                            34.7 |                120.0% |
|       Lee |                   11.4 |                            34.0 |                769.8% |
|     Scott |                   56.3 |                            32.5 |                121.5% |
|  Cherokee |                    3.6 |                            31.8 |                 39.1% |
|   Kossuth |                    4.6 |                            30.9 |                 34.5% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                   11.4 |                            34.0 |                769.8% |
|      Jasper |                   11.1 |                            30.0 |                193.1% |
|     Osceola |                    3.0 |                            50.4 |                133.4% |
|       Scott |                   56.3 |                            32.5 |                121.5% |
|     Guthrie |                    3.7 |                            34.7 |                120.0% |
|      Shelby |                    4.0 |                            34.9 |                105.8% |
|     Dubuque |                   16.4 |                            16.9 |                 93.7% |
|       Emmet |                    5.3 |                            57.4 |                 83.3% |
| Cerro Gordo |                    4.7 |                            11.1 |                 81.8% |
|      Benton |                    2.6 |                            10.0 |                 78.6% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Adair |                    0.3 |                             4.0 |               \-47.1% |
| Poweshiek |                    0.4 |                             2.3 |               \-44.4% |
|   Wapello |                    4.0 |                            11.4 |               \-41.7% |
| Chickasaw |                    0.1 |                             1.2 |               \-38.4% |
|    Monroe |                    0.1 |                             1.9 |               \-38.4% |
|  Crawford |                    1.1 |                             6.8 |               \-37.5% |
|   Calhoun |                    0.7 |                             7.4 |               \-36.8% |
|    Butler |                    0.4 |                             3.0 |               \-33.3% |
|     Lucas |                    0.4 |                             5.0 |               \-33.3% |
|  Harrison |                    1.1 |                             8.1 |               \-31.8% |
