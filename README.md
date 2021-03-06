Compiled at 2021-03-06 23:58:54 UTC

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

## Tables as of 2021-03-05

As of 2021-03-05, IPDH is reporting 943 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  100.3 |                            20.5 |               \-11.2% |
|          Linn |                   21.0 |                             9.3 |                \-4.9% |
|         Scott |                   24.1 |                            14.0 |                 18.9% |
|       Johnson |                   17.4 |                            11.5 |                \-7.2% |
|    Black Hawk |                   15.1 |                            11.5 |                  0.9% |
|      Woodbury |                   21.9 |                            21.2 |                 13.5% |
|       Dubuque |                   14.4 |                            14.8 |               \-30.3% |
|         Story |                   21.9 |                            22.5 |                 21.2% |
|        Dallas |                   21.4 |                            22.9 |               \-12.3% |
| Pottawattamie |                   16.0 |                            17.2 |                  8.2% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.3 |                            51.0 |                130.8% |
| Allamakee |                    6.6 |                            48.0 |                194.5% |
|   O’Brien |                    6.0 |                            43.6 |                 96.0% |
|      Cass |                    4.6 |                            35.6 |                 50.0% |
|     Lucas |                    3.0 |                            34.9 |                115.4% |
|   Wapello |                   11.9 |                            33.9 |                \-9.1% |
|    Shelby |                    3.9 |                            33.7 |                 88.9% |
|    Bremer |                    8.0 |                            31.9 |                142.3% |
|     Cedar |                    5.9 |                            31.4 |                 11.6% |
|    Jasper |                   11.6 |                            31.1 |               \-19.3% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Allamakee |                    6.6 |                            48.0 |                194.5% |
| Chickasaw |                    2.4 |                            20.4 |                166.6% |
|    Bremer |                    8.0 |                            31.9 |                142.3% |
|     Wayne |                    3.3 |                            51.0 |                130.8% |
|     Lucas |                    3.0 |                            34.9 |                115.4% |
|       Ida |                    1.4 |                            20.8 |                112.5% |
|   Audubon |                    1.4 |                            26.0 |                112.5% |
|   O’Brien |                    6.0 |                            43.6 |                 96.0% |
|  Delaware |                    2.0 |                            11.8 |                 91.0% |
|    Shelby |                    3.9 |                            33.7 |                 88.9% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    2.4 |                            16.1 |               \-69.6% |
|        Lee |                    2.6 |                             7.6 |               \-52.8% |
|  Appanoose |                    1.1 |                             9.2 |               \-51.6% |
|      Henry |                    1.0 |                             5.0 |               \-48.1% |
|       Lyon |                    0.4 |                             3.6 |               \-47.3% |
|   Hamilton |                    0.7 |                             4.8 |               \-45.5% |
|     Grundy |                    1.3 |                            10.5 |               \-40.7% |
|     Louisa |                    0.9 |                             7.8 |               \-38.1% |
| Des Moines |                    5.1 |                            13.2 |               \-36.8% |
|     Howard |                    1.0 |                            10.9 |               \-33.3% |
