Compiled at 2021-03-09 18:06:57 UTC

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

## Tables as of 2021-03-09

As of 2021-03-09, IPDH is reporting 516 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  104.7 |                            21.4 |                \-4.0% |
|          Linn |                   17.1 |                             7.6 |               \-23.0% |
|         Scott |                   23.4 |                            13.5 |                 11.0% |
|       Johnson |                   16.1 |                            10.7 |               \-13.7% |
|    Black Hawk |                   14.9 |                            11.3 |                  6.7% |
|      Woodbury |                   23.0 |                            22.3 |                 23.5% |
|       Dubuque |                   10.9 |                            11.2 |               \-43.9% |
|         Story |                   20.6 |                            21.2 |                  6.3% |
|        Dallas |                   19.9 |                            21.2 |               \-19.8% |
| Pottawattamie |                   15.7 |                            16.9 |                  4.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.7 |                            57.7 |                266.6% |
| Allamakee |                    6.3 |                            45.9 |                 75.9% |
|   O’Brien |                    6.1 |                            44.7 |                 78.6% |
|       Ida |                    3.0 |                            43.7 |                179.9% |
|   Madison |                    6.7 |                            41.1 |                 58.8% |
|      Cass |                    4.7 |                            36.7 |                 53.9% |
|    Shelby |                    3.7 |                            32.4 |                 73.7% |
|       Sac |                    3.0 |                            30.9 |                 47.4% |
|  Cherokee |                    3.4 |                            30.5 |                158.4% |
|   Wapello |                   10.4 |                            29.8 |               \-27.9% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Wayne |                    3.7 |                            57.7 |                266.6% |
|      Clay |                    4.0 |                            25.0 |                218.3% |
|       Ida |                    3.0 |                            43.7 |                179.9% |
|  Cherokee |                    3.4 |                            30.5 |                158.4% |
|   Fayette |                    4.0 |                            20.4 |                105.8% |
|     Floyd |                    2.4 |                            15.5 |                 84.7% |
|   O’Brien |                    6.1 |                            44.7 |                 78.6% |
|  Humboldt |                    2.3 |                            23.9 |                 77.0% |
| Allamakee |                    6.3 |                            45.9 |                 75.9% |
|    Shelby |                    3.7 |                            32.4 |                 73.7% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                    1.4 |                             4.2 |               \-62.2% |
|      Jasper |                    6.3 |                            16.9 |               \-60.2% |
|   Appanoose |                    1.0 |                             8.0 |               \-53.3% |
|     Dubuque |                   10.9 |                            11.2 |               \-43.9% |
|      Louisa |                    0.9 |                             7.8 |               \-40.9% |
|  Des Moines |                    4.4 |                            11.4 |               \-38.7% |
|        Lyon |                    0.7 |                             6.1 |               \-36.8% |
| Buena Vista |                    4.0 |                            20.4 |               \-36.4% |
|    Hamilton |                    0.6 |                             3.9 |               \-31.3% |
|        Tama |                    2.4 |                            14.4 |               \-29.4% |
