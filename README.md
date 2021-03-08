Compiled at 2021-03-08 20:18:58 UTC

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

## Tables as of 2021-03-08

As of 2021-03-08, IPDH is reporting 485 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   93.9 |                            19.1 |               \-12.5% |
|          Linn |                   17.7 |                             7.8 |               \-18.1% |
|         Scott |                   22.3 |                            12.9 |                  5.8% |
|       Johnson |                   16.3 |                            10.8 |                \-9.7% |
|    Black Hawk |                   14.0 |                            10.7 |                  1.9% |
|      Woodbury |                   20.6 |                            20.0 |                 10.2% |
|       Dubuque |                   12.1 |                            12.5 |               \-34.8% |
|         Story |                   18.7 |                            19.3 |                  0.0% |
|        Dallas |                   17.7 |                            19.0 |               \-28.8% |
| Pottawattamie |                   15.3 |                            16.4 |                  3.6% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.7 |                            57.7 |                200.1% |
| Allamakee |                    6.0 |                            43.8 |                 81.5% |
|   O’Brien |                    5.9 |                            42.6 |                 84.6% |
|      Cass |                    4.6 |                            35.6 |                 50.0% |
|     Lucas |                    2.7 |                            31.6 |                 62.5% |
|       Ida |                    2.1 |                            31.2 |                144.4% |
|    Shelby |                    3.6 |                            31.2 |                 68.4% |
|  Cherokee |                    3.1 |                            28.0 |                141.7% |
|   Wapello |                    9.7 |                            27.8 |               \-32.4% |
|     Cedar |                    4.7 |                            25.3 |                \-9.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.7 |                            57.7 |                200.1% |
|       Ida |                    2.1 |                            31.2 |                144.4% |
|  Cherokee |                    3.1 |                            28.0 |                141.7% |
|   Fayette |                    3.7 |                            18.9 |                106.2% |
| Chickasaw |                    2.0 |                            16.8 |                 91.0% |
|   O’Brien |                    5.9 |                            42.6 |                 84.6% |
| Allamakee |                    6.0 |                            43.8 |                 81.5% |
|      Clay |                    2.3 |                            14.3 |                 77.0% |
|    Shelby |                    3.6 |                            31.2 |                 68.4% |
|     Lucas |                    2.7 |                            31.6 |                 62.5% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                    5.6 |                            15.0 |               \-65.4% |
|         Lee |                    1.7 |                             5.1 |               \-57.8% |
|        Page |                    2.0 |                            13.2 |               \-56.2% |
|      Louisa |                    0.6 |                             5.2 |               \-50.0% |
|   Appanoose |                    1.1 |                             9.2 |               \-48.3% |
|  Des Moines |                    4.3 |                            11.0 |               \-40.3% |
| Buena Vista |                    3.7 |                            18.9 |               \-37.7% |
|    Harrison |                    1.1 |                             8.1 |               \-37.5% |
|      Clarke |                    1.1 |                            12.2 |               \-37.5% |
|        Lyon |                    0.7 |                             6.1 |               \-36.8% |
