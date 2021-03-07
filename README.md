Compiled at 2021-03-07 20:16:38 UTC

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

## Tables as of 2021-03-07

As of 2021-03-07, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   87.9 |                            17.9 |               \-18.4% |
|          Linn |                   18.4 |                             8.1 |                \-8.1% |
|         Scott |                   20.0 |                            11.6 |                \-7.5% |
|       Johnson |                   14.9 |                             9.8 |               \-19.6% |
|    Black Hawk |                   14.3 |                            10.9 |                  2.9% |
|      Woodbury |                   19.7 |                            19.1 |                 11.5% |
|       Dubuque |                   12.0 |                            12.3 |               \-38.9% |
|         Story |                   18.9 |                            19.4 |                  0.7% |
|        Dallas |                   18.1 |                            19.4 |               \-26.0% |
| Pottawattamie |                   13.4 |                            14.4 |                \-9.8% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.3 |                            51.0 |                172.8% |
|   O’Brien |                    5.9 |                            42.6 |                 84.6% |
| Allamakee |                    5.6 |                            40.7 |                100.0% |
|     Lucas |                    3.0 |                            34.9 |                133.4% |
|      Cass |                    4.3 |                            33.4 |                 48.0% |
|    Shelby |                    3.6 |                            31.2 |                 68.4% |
|     Cedar |                    5.1 |                            27.6 |                \-2.3% |
|  Cherokee |                    2.9 |                            25.4 |                 58.8% |
| Dickinson |                    4.3 |                            24.8 |                 37.0% |
|   Wapello |                    8.6 |                            24.5 |               \-38.5% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.3 |                            51.0 |                172.8% |
|     Lucas |                    3.0 |                            34.9 |                133.4% |
| Chickasaw |                    2.1 |                            18.0 |                100.1% |
| Allamakee |                    5.6 |                            40.7 |                100.0% |
|   Fayette |                    3.4 |                            17.4 |                 93.7% |
|  Delaware |                    2.0 |                            11.8 |                 91.0% |
|       Ida |                    1.4 |                            20.8 |                 88.9% |
|    Butler |                    2.4 |                            16.8 |                 84.7% |
|   O’Brien |                    5.9 |                            42.6 |                 84.6% |
|    Shelby |                    3.6 |                            31.2 |                 68.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    5.0 |                            13.4 |               \-70.8% |
|        Lee |                    1.7 |                             5.1 |               \-59.6% |
|  Appanoose |                    0.9 |                             6.9 |               \-56.7% |
|       Page |                    2.1 |                            14.2 |               \-53.2% |
|     Clarke |                    1.0 |                            10.6 |               \-48.1% |
|     Louisa |                    0.6 |                             5.2 |               \-47.6% |
|       Lyon |                    0.4 |                             3.6 |               \-47.3% |
| Des Moines |                    4.1 |                            10.6 |               \-46.3% |
|   Hamilton |                    0.7 |                             4.8 |               \-42.9% |
|    Dubuque |                   12.0 |                            12.3 |               \-38.9% |
