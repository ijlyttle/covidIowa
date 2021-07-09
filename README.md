Compiled at 2021-07-09 23:55:51 UTC

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

## Tables as of 2021-07-09

As of 2021-07-09, IPDH is reporting 130 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   37.6 |                             7.7 |                264.9% |
|          Linn |                   11.3 |                             5.0 |                126.3% |
|         Scott |                    1.0 |                             0.6 |               \-50.0% |
|       Johnson |                    3.7 |                             2.5 |                 10.0% |
|    Black Hawk |                   19.0 |                            14.5 |                 33.3% |
|      Woodbury |                  \-1.6 |                           \-1.5 |              \-118.2% |
|       Dubuque |                    3.7 |                             3.8 |                 37.5% |
|         Story |                    6.4 |                             6.6 |                225.0% |
|        Dallas |                   10.6 |                            11.3 |                523.1% |
| Pottawattamie |                    1.0 |                             1.1 |               \-22.2% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.9 |                           109.9 |              2 154.0% |
|    Decatur |                    3.4 |                            43.6 |                209.9% |
|    Fremont |                    2.7 |                            39.0 |                271.4% |
|      Henry |                    7.3 |                            36.5 |                544.3% |
|     Keokuk |                    3.1 |                            30.7 |                189.9% |
|   Franklin |                    2.7 |                            27.0 |                136.4% |
|   Humboldt |                    2.6 |                            26.9 |                 56.2% |
|     Monroe |                    2.0 |                            26.0 |                200.0% |
| Montgomery |                    2.3 |                            23.1 |                228.6% |
|      Wayne |                    1.4 |                            22.2 |                 30.8% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.9 |                           109.9 |              2 154.0% |
|      Henry |                    7.3 |                            36.5 |                544.3% |
|     Dallas |                   10.6 |                            11.3 |                523.1% |
|    Fremont |                    2.7 |                            39.0 |                271.4% |
|       Polk |                   37.6 |                             7.7 |                264.9% |
| Montgomery |                    2.3 |                            23.1 |                228.6% |
|      Story |                    6.4 |                             6.6 |                225.0% |
|    Decatur |                    3.4 |                            43.6 |                209.9% |
|     Monona |                    1.6 |                            18.2 |                200.0% |
|     Monroe |                    2.0 |                            26.0 |                200.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.0 |                          \-18.5 |              \-275.0% |
|   Mahaska |                  \-2.7 |                          \-12.3 |              \-250.0% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Carroll |                  \-2.4 |                          \-12.0 |              \-211.1% |
|    Shelby |                  \-1.6 |                          \-13.7 |              \-150.0% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-125.0% |
|  Woodbury |                  \-1.6 |                           \-1.5 |              \-118.2% |
|     Union |                  \-1.1 |                           \-9.3 |              \-114.3% |
|     Worth |                  \-1.1 |                          \-15.5 |              \-112.5% |
|   Audubon |                  \-1.0 |                          \-18.2 |              \-100.0% |
