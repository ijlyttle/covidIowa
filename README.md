Compiled at 2021-03-10 17:54:54 UTC

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

## Tables as of 2021-03-10

As of 2021-03-10, IPDH is reporting 800 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  118.3 |                            24.1 |                 19.1% |
|          Linn |                   17.1 |                             7.6 |               \-16.4% |
|         Scott |                   29.1 |                            16.9 |                 47.6% |
|       Johnson |                   16.4 |                            10.9 |                \-3.9% |
|    Black Hawk |                   17.4 |                            13.3 |                 27.7% |
|      Woodbury |                   26.7 |                            25.9 |                 40.6% |
|       Dubuque |                   12.4 |                            12.8 |               \-29.8% |
|         Story |                   22.6 |                            23.2 |                 34.1% |
|        Dallas |                   20.7 |                            22.2 |               \-13.6% |
| Pottawattamie |                   17.7 |                            19.0 |                 23.6% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.4 |                            64.6 |                279.9% |
|     Wayne |                    3.9 |                            59.9 |                239.9% |
| Allamakee |                    6.3 |                            45.9 |                 82.1% |
|   Madison |                    7.0 |                            42.8 |                 80.6% |
|   O’Brien |                    5.1 |                            37.4 |                 30.3% |
|  Cherokee |                    4.0 |                            35.6 |                 94.5% |
|       Sac |                    3.4 |                            35.3 |                 47.6% |
|    Shelby |                    4.0 |                            34.9 |                 40.0% |
|      Clay |                    5.6 |                            34.8 |                228.5% |
| Palo Alto |                    3.0 |                            33.8 |                 86.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.4 |                            64.6 |                279.9% |
|     Wayne |                    3.9 |                            59.9 |                239.9% |
|      Clay |                    5.6 |                            34.8 |                228.5% |
|  Cherokee |                    4.0 |                            35.6 |                 94.5% |
|  Mitchell |                    2.9 |                            27.0 |                 92.9% |
| Palo Alto |                    3.0 |                            33.8 |                 86.7% |
| Allamakee |                    6.3 |                            45.9 |                 82.1% |
|   Madison |                    7.0 |                            42.8 |                 80.6% |
|  Marshall |                    7.9 |                            20.0 |                 77.1% |
|     Floyd |                    2.7 |                            17.4 |                 73.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                    1.3 |                             3.8 |               \-60.0% |
|      Jasper |                    7.4 |                            20.0 |               \-53.9% |
| Buena Vista |                    3.7 |                            18.9 |               \-38.9% |
|    Hamilton |                    0.6 |                             3.9 |               \-38.9% |
|     Osceola |                    0.6 |                             9.6 |               \-35.3% |
|     Dubuque |                   12.4 |                            12.8 |               \-29.8% |
|   Appanoose |                    0.7 |                             5.7 |               \-25.0% |
|  Pocahontas |                    0.3 |                             4.3 |               \-25.0% |
|   Winnebago |                    1.7 |                            16.6 |               \-24.0% |
|      Clarke |                    1.4 |                            15.2 |               \-22.7% |
