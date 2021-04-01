Compiled at 2021-04-01 00:02:32 UTC

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

## Tables as of 2021-03-31

As of 2021-03-31, IPDH is reporting 1105 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  125.4 |                            25.6 |                 35.9% |
|          Linn |                   18.4 |                             8.1 |                 11.5% |
|         Scott |                   64.4 |                            37.3 |                119.1% |
|       Johnson |                   27.0 |                            17.9 |                 88.5% |
|    Black Hawk |                   16.7 |                            12.7 |                 55.0% |
|      Woodbury |                   33.9 |                            32.8 |                 20.2% |
|       Dubuque |                   20.1 |                            20.7 |                108.4% |
|         Story |                   27.1 |                            27.9 |                 97.0% |
|        Dallas |                   25.9 |                            27.7 |                 62.1% |
| Pottawattamie |                   25.6 |                            27.4 |                 55.0% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   12.6 |                            72.8 |                 43.9% |
|     Emmet |                    5.7 |                            62.1 |                 95.8% |
|      Clay |                    9.3 |                            58.0 |                 26.3% |
|   Osceola |                    2.9 |                            48.0 |                 68.7% |
|    Shelby |                    5.0 |                            43.7 |                250.1% |
| Palo Alto |                    3.7 |                            41.8 |                 73.7% |
|     Scott |                   64.4 |                            37.3 |                119.1% |
|   Guthrie |                    3.9 |                            36.1 |                 41.6% |
|   Kossuth |                    5.3 |                            35.7 |                 51.7% |
|       Lee |                   11.9 |                            35.2 |                718.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                   11.9 |                            35.2 |                718.4% |
|      Shelby |                    5.0 |                            43.7 |                250.1% |
| Cerro Gordo |                    7.1 |                            16.8 |                171.4% |
|      Jasper |                   11.7 |                            31.5 |                161.8% |
|       Cedar |                    4.0 |                            21.5 |                150.0% |
|       Scott |                   64.4 |                            37.3 |                119.1% |
|     Dubuque |                   20.1 |                            20.7 |                108.4% |
|     Clinton |                   12.6 |                            27.1 |                106.5% |
|      Benton |                    3.0 |                            11.7 |                100.0% |
|       Story |                   27.1 |                            27.9 |                 97.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Crawford |                    0.9 |                             5.1 |               \-48.0% |
|  Harrison |                    0.9 |                             6.1 |               \-40.9% |
| Poweshiek |                    0.4 |                             2.3 |               \-37.5% |
|    Butler |                    0.4 |                             3.0 |               \-37.5% |
|     Adair |                    0.4 |                             6.0 |               \-37.5% |
|   Calhoun |                    0.7 |                             7.4 |               \-36.8% |
|    Howard |                    0.6 |                             6.2 |               \-35.3% |
|     Wayne |                    1.1 |                            17.7 |               \-34.8% |
|   Wapello |                    4.7 |                            13.5 |               \-34.4% |
|     Lucas |                    0.4 |                             5.0 |               \-33.3% |
