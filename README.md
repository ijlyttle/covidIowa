Compiled at 2021-03-12 22:13:01 UTC

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

## Tables as of 2021-03-12

As of 2021-03-12, IPDH is reporting 489 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |
| 2021-03-05 |                  543.3 |                            17.2 |                  0.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  108.3 |                            22.1 |                 12.7% |
|          Linn |                   13.7 |                             6.0 |               \-28.5% |
|         Scott |                   28.0 |                            16.2 |                 47.1% |
|       Johnson |                   13.0 |                             8.6 |               \-22.8% |
|    Black Hawk |                   16.0 |                            12.2 |                 20.2% |
|      Woodbury |                   27.0 |                            26.2 |                 43.1% |
|       Dubuque |                    9.6 |                             9.8 |               \-24.5% |
|         Story |                   18.6 |                            19.1 |                \-3.5% |
|        Dallas |                   19.0 |                            20.3 |               \-14.1% |
| Pottawattamie |                   17.7 |                            19.0 |                 52.3% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.7 |                            68.7 |                166.6% |
|     Wayne |                    3.9 |                            59.9 |                112.5% |
| Dickinson |                    7.9 |                            45.5 |                121.4% |
|   Madison |                    6.9 |                            42.0 |                139.1% |
|      Clay |                    6.7 |                            41.9 |                217.6% |
| Allamakee |                    5.3 |                            38.6 |                 12.8% |
|  Cherokee |                    4.1 |                            36.9 |                 71.4% |
|      Page |                    5.4 |                            35.9 |                 66.7% |
|   Wapello |                   10.0 |                            28.6 |               \-18.1% |
| Palo Alto |                    2.4 |                            27.3 |                 14.3% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Clay |                    6.7 |                            41.9 |                217.6% |
|       Ida |                    4.7 |                            68.7 |                166.6% |
|   Madison |                    6.9 |                            42.0 |                139.1% |
| Dickinson |                    7.9 |                            45.5 |                121.4% |
|     Wayne |                    3.9 |                            59.9 |                112.5% |
|     Jones |                    2.0 |                             9.7 |                 91.0% |
|  Franklin |                    1.4 |                            14.2 |                 88.9% |
|     Adair |                    1.9 |                            26.0 |                 81.9% |
|     Mills |                    3.1 |                            20.8 |                 81.2% |
|    Monona |                    1.6 |                            18.2 |                 79.9% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                    0.6 |                             1.7 |               \-65.6% |
|      Jasper |                    6.7 |                            18.1 |               \-56.5% |
|      Keokuk |                    0.3 |                             2.8 |               \-50.0% |
| Buena Vista |                    2.6 |                            13.1 |               \-47.9% |
|        Tama |                    1.6 |                             9.3 |               \-45.5% |
|       Worth |                    0.4 |                             5.8 |               \-44.4% |
|      Bremer |                    3.9 |                            15.4 |               \-43.3% |
|   Chickasaw |                    0.7 |                             6.0 |               \-42.9% |
|   Appanoose |                    0.4 |                             3.5 |               \-41.2% |
|   Jefferson |                    0.9 |                             4.7 |               \-38.1% |
