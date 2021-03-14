Compiled at 2021-03-14 20:17:37 UTC

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

## Tables as of 2021-03-14

As of 2021-03-14, IPDH is reporting 282 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |
| 2021-03-08 |                  483.1 |                            15.3 |                \-9.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  107.4 |                            21.9 |                 22.0% |
|          Linn |                   14.7 |                             6.5 |               \-19.1% |
|         Scott |                   25.1 |                            14.5 |                 24.5% |
|       Johnson |                   11.4 |                             7.6 |               \-21.6% |
|    Black Hawk |                   16.4 |                            12.5 |                 14.0% |
|      Woodbury |                   30.6 |                            29.6 |                 52.4% |
|       Dubuque |                    8.6 |                             8.8 |               \-26.4% |
|         Story |                   15.9 |                            16.3 |               \-15.1% |
|        Dallas |                   20.6 |                            22.0 |                 12.7% |
| Pottawattamie |                   15.1 |                            16.2 |                 11.9% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.9 |                            70.8 |                141.1% |
|      Clay |                    7.1 |                            44.6 |                171.4% |
|  Cherokee |                    5.0 |                            44.5 |                 55.6% |
| Dickinson |                    7.6 |                            43.9 |                 62.1% |
|     Wayne |                    2.6 |                            39.9 |               \-16.7% |
|   Madison |                    5.7 |                            35.0 |                 67.9% |
|      Page |                    5.1 |                            34.0 |                 95.5% |
|   Wapello |                   10.4 |                            29.8 |                 19.4% |
|  Woodbury |                   30.6 |                            29.6 |                 52.4% |
|    Shelby |                    3.0 |                            26.2 |               \-12.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Clay |                    7.1 |                            44.6 |                171.4% |
|       Lyon |                    2.7 |                            23.1 |                159.9% |
|        Ida |                    4.9 |                            70.8 |                141.1% |
|    Carroll |                    4.6 |                            22.7 |                129.4% |
|       Page |                    5.1 |                            34.0 |                 95.5% |
|      Mills |                    2.7 |                            18.0 |                 73.3% |
| Washington |                    2.4 |                            11.1 |                 71.4% |
|    Madison |                    5.7 |                            35.0 |                 67.9% |
|  Dickinson |                    7.6 |                            43.9 |                 62.1% |
|      Jones |                    2.0 |                             9.7 |                 61.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Fremont |                  \-0.1 |                           \-2.1 |               \-57.2% |
|  Chickasaw |                    0.4 |                             3.6 |               \-54.5% |
|       Tama |                    1.1 |                             6.8 |               \-51.6% |
|     Butler |                    0.7 |                             4.9 |               \-50.0% |
|     Keokuk |                    0.3 |                             2.8 |               \-50.0% |
|      Worth |                    0.3 |                             3.9 |               \-50.0% |
|    Fayette |                    1.3 |                             6.5 |               \-48.4% |
|    Audubon |                    0.1 |                             2.6 |               \-42.8% |
| Montgomery |                    0.0 |                             0.0 |               \-41.7% |
|    O’Brien |                    3.3 |                            23.9 |               \-37.5% |
