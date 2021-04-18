Compiled at 2021-04-18 20:19:20 UTC

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

## Tables as of 2021-04-18

As of 2021-04-18, IPDH is reporting 706 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   74.0 |                            15.1 |               \-16.5% |
|          Linn |                   20.9 |                             9.2 |               \-17.7% |
|         Scott |                   58.1 |                            33.6 |                  1.0% |
|       Johnson |                   28.0 |                            18.5 |                \-2.4% |
|    Black Hawk |                   14.4 |                            11.0 |               \-15.0% |
|      Woodbury |                   17.7 |                            17.2 |               \-17.6% |
|       Dubuque |                   19.7 |                            20.3 |               \-28.2% |
|         Story |                    9.6 |                             9.9 |               \-31.5% |
|        Dallas |                   11.1 |                            11.9 |               \-16.7% |
| Pottawattamie |                   19.9 |                            21.3 |               \-18.4% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    2.6 |                            43.2 |                  8.7% |
|         Scott |                   58.1 |                            33.6 |                  1.0% |
|     Dickinson |                    5.1 |                            29.8 |               \-38.6% |
|         Emmet |                    2.4 |                            26.4 |               \-14.3% |
|        Shelby |                    3.0 |                            26.2 |                \-6.7% |
|          Clay |                    4.1 |                            25.9 |               \-28.0% |
|           Ida |                    1.7 |                            25.0 |                 26.6% |
|     Palo Alto |                    2.0 |                            22.5 |               \-12.5% |
|           Sac |                    2.1 |                            22.0 |                 37.5% |
| Pottawattamie |                   19.9 |                            21.3 |               \-18.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Pocahontas |                    1.0 |                            15.1 |                100.0% |
|  Appanoose |                    1.1 |                             9.2 |                 66.6% |
|    Madison |                    3.0 |                            18.4 |                 64.7% |
|    Webster |                    3.1 |                             8.8 |                 61.1% |
|   Hamilton |                    1.7 |                            11.6 |                 58.3% |
|     Benton |                    2.0 |                             7.8 |                 50.0% |
|    Guthrie |                    1.7 |                            16.0 |                 46.1% |
|        Sac |                    2.1 |                            22.0 |                 37.5% |
|       Iowa |                    1.3 |                             7.9 |                 33.4% |
|  Jefferson |                    0.7 |                             3.9 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                    1.7 |                             8.5 |               \-55.8% |
|      Marion |                    0.9 |                             2.6 |               \-51.9% |
|     Wapello |                    1.1 |                             3.3 |               \-44.4% |
|       Davis |                    0.1 |                             1.6 |               \-42.8% |
|    Delaware |                    2.9 |                            16.8 |               \-42.6% |
| Cerro Gordo |                    4.6 |                            10.8 |               \-41.8% |
|    Cherokee |                    1.0 |                             8.9 |               \-39.1% |
|   Dickinson |                    5.1 |                            29.8 |               \-38.6% |
|        Page |                    2.0 |                            13.2 |               \-38.2% |
|  Washington |                    2.0 |                             9.1 |               \-36.4% |
