Compiled at 2021-04-27 17:13:52 UTC

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

## Tables as of 2021-04-27

As of 2021-04-27, IPDH is reporting 346 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   75.4 |                            15.4 |                \-0.7% |
|          Linn |                   23.6 |                            10.4 |               \-10.4% |
|         Scott |                   34.9 |                            20.2 |               \-38.2% |
|       Johnson |                   20.9 |                            13.8 |               \-30.8% |
|    Black Hawk |                   11.0 |                             8.4 |               \-27.6% |
|      Woodbury |                   12.9 |                            12.5 |               \-28.1% |
|       Dubuque |                    9.0 |                             9.2 |               \-50.0% |
|         Story |                   12.7 |                            13.1 |                 11.6% |
|        Dallas |                   13.0 |                            13.9 |                 14.0% |
| Pottawattamie |                   17.4 |                            18.7 |               \-16.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|   Winnebago |                    3.4 |                            33.1 |                 63.2% |
|       Emmet |                    2.9 |                            31.0 |                  0.0% |
|     Osceola |                    1.7 |                            28.8 |               \-32.2% |
|       Floyd |                    3.9 |                            24.7 |                 70.0% |
|  Pocahontas |                    1.6 |                            23.7 |                 20.0% |
| Cerro Gordo |                    9.4 |                            22.2 |                 55.3% |
|    Delaware |                    3.7 |                            21.8 |                 13.8% |
|      Warren |                   11.0 |                            21.4 |                \-3.5% |
|    Franklin |                    2.1 |                            21.3 |                 83.4% |
|      Hardin |                    3.6 |                            21.2 |                 52.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                    0.4 |                             3.5 |                899.3% |
| Washington |                    2.4 |                            11.1 |                100.1% |
|      Lucas |                    1.6 |                            18.3 |                 99.9% |
|   Franklin |                    2.1 |                            21.3 |                 83.4% |
|     Jasper |                    3.6 |                             9.6 |                 77.8% |
| Des Moines |                    6.7 |                            17.2 |                 74.2% |
|      Davis |                    0.7 |                             7.9 |                 71.4% |
|     Marion |                    3.1 |                             9.5 |                 70.6% |
|      Floyd |                    3.9 |                            24.7 |                 70.0% |
|     Howard |                    1.1 |                            12.5 |                 66.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Plymouth |                    1.1 |                             4.5 |               \-65.1% |
|     Shelby |                    0.4 |                             3.7 |               \-64.3% |
| Winneshiek |                    0.9 |                             4.3 |               \-55.2% |
|     Grundy |                    0.0 |                             0.0 |               \-53.3% |
|    Dubuque |                    9.0 |                             9.2 |               \-50.0% |
|    Clayton |                    0.6 |                             3.3 |               \-50.0% |
|    Fremont |                    0.1 |                             2.1 |               \-38.4% |
|      Scott |                   34.9 |                            20.2 |               \-38.2% |
|      Sioux |                    2.7 |                             7.8 |               \-38.1% |
|  Palo Alto |                    0.9 |                             9.6 |               \-38.1% |
