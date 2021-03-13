Compiled at 2021-03-13 23:57:26 UTC

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

## Tables as of 2021-03-13

As of 2021-03-13, IPDH is reporting 551 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |
| 2021-03-07 |                  463.6 |                            14.7 |               \-14.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   97.3 |                            19.8 |                \-3.0% |
|          Linn |                   13.0 |                             5.7 |               \-36.4% |
|         Scott |                   22.3 |                            12.9 |                \-7.4% |
|       Johnson |                   11.4 |                             7.6 |               \-32.6% |
|    Black Hawk |                   14.7 |                            11.2 |                \-2.7% |
|      Woodbury |                   28.6 |                            27.7 |                 29.4% |
|       Dubuque |                    8.0 |                             8.2 |               \-41.7% |
|         Story |                   15.3 |                            15.7 |               \-28.7% |
|        Dallas |                   18.6 |                            19.9 |               \-12.7% |
| Pottawattamie |                   13.0 |                            13.9 |               \-17.6% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.9 |                            70.8 |                141.1% |
|      Clay |                    7.0 |                            43.7 |                166.7% |
| Dickinson |                    7.4 |                            43.0 |                 47.5% |
|  Cherokee |                    4.7 |                            42.0 |                 48.1% |
|     Wayne |                    2.4 |                            37.7 |               \-20.0% |
|   Madison |                    5.6 |                            34.1 |                 43.8% |
|      Page |                    5.0 |                            33.1 |                 75.0% |
|   Wapello |                    9.9 |                            28.2 |               \-15.6% |
|  Woodbury |                   28.6 |                            27.7 |                 29.4% |
|       Sac |                    2.4 |                            25.0 |                  4.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Clay |                    7.0 |                            43.7 |                166.7% |
|       Lyon |                    2.7 |                            23.1 |                159.9% |
|        Ida |                    4.9 |                            70.8 |                141.1% |
|    Carroll |                    3.9 |                            19.1 |                 88.9% |
|       Page |                    5.0 |                            33.1 |                 75.0% |
|      Mills |                    2.6 |                            17.0 |                 66.6% |
| Washington |                    2.4 |                            11.1 |                 60.0% |
|     Monona |                    1.4 |                            16.6 |                 54.6% |
|   Cherokee |                    4.7 |                            42.0 |                 48.1% |
|  Dickinson |                    7.4 |                            43.0 |                 47.5% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Chickasaw |                    0.4 |                             3.6 |               \-58.3% |
|   Fremont |                  \-0.1 |                           \-2.1 |               \-57.2% |
|   Fayette |                    1.0 |                             5.1 |               \-56.2% |
|    Keokuk |                    0.1 |                             1.4 |               \-55.5% |
|      Tama |                    1.1 |                             6.8 |               \-53.1% |
|   Audubon |                    0.1 |                             2.6 |               \-52.9% |
|     Worth |                    0.3 |                             3.9 |               \-52.6% |
|       Lee |                    0.7 |                             2.1 |               \-52.0% |
|    Butler |                    0.7 |                             4.9 |               \-50.0% |
|    Bremer |                    3.6 |                            14.2 |               \-49.2% |
