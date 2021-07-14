Compiled at 2021-07-14 23:53:51 UTC

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

## Tables as of 2021-07-14

As of 2021-07-14, IPDH is reporting 202 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   44.1 |                             9.0 |                345.1% |
|          Linn |                   12.3 |                             5.4 |                181.8% |
|         Scott |                    4.4 |                             2.6 |                 65.2% |
|       Johnson |                    3.7 |                             2.5 |                 26.9% |
|    Black Hawk |                   22.0 |                            16.8 |                 67.7% |
|      Woodbury |                    0.4 |                             0.4 |               \-44.4% |
|       Dubuque |                    4.6 |                             4.7 |                178.5% |
|         Story |                    7.3 |                             7.5 |                383.4% |
|        Dallas |                   12.3 |                            13.1 |                745.7% |
| Pottawattamie |                    2.4 |                             2.6 |                 14.3% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.7 |                           109.5 |              1 985.7% |
|    Decatur |                    3.6 |                            45.4 |                166.7% |
|    Fremont |                    2.7 |                            39.0 |                188.8% |
|     Monroe |                    2.9 |                            37.1 |                285.7% |
|      Henry |                    6.7 |                            33.6 |                350.1% |
|     Keokuk |                    3.4 |                            33.5 |                244.4% |
| Montgomery |                    3.0 |                            30.3 |                250.0% |
|   Humboldt |                    2.7 |                            28.4 |                100.0% |
|   Franklin |                    2.9 |                            28.4 |                 80.0% |
|    Webster |                   10.1 |                            28.2 |                 81.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   40.7 |                           109.5 |              1 985.7% |
|      Dallas |                   12.3 |                            13.1 |                745.7% |
|       Story |                    7.3 |                             7.5 |                383.4% |
|       Henry |                    6.7 |                            33.6 |                350.1% |
|        Polk |                   44.1 |                             9.0 |                345.1% |
| Buena Vista |                    3.0 |                            15.3 |                300.0% |
|      Monroe |                    2.9 |                            37.1 |                285.7% |
|     Madison |                    3.3 |                            20.1 |                275.0% |
|  Washington |                    3.0 |                            13.7 |                250.0% |
|  Montgomery |                    3.0 |                            30.3 |                250.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.1 |                          \-19.4 |              \-287.5% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Mahaska |                  \-3.4 |                          \-15.5 |              \-206.3% |
|   Carroll |                  \-2.0 |                           \-9.9 |              \-200.0% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-128.6% |
|    Shelby |                  \-1.3 |                          \-11.2 |              \-116.7% |
|     Worth |                  \-1.1 |                          \-15.5 |              \-111.1% |
|   Audubon |                  \-1.1 |                          \-20.8 |              \-110.0% |
|     Mills |                  \-1.0 |                           \-6.6 |              \-100.0% |
|     Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
