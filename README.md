Compiled at 2021-07-12 17:32:46 UTC

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

## Tables as of 2021-07-12

As of 2021-07-12, IPDH is reporting 57 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   39.7 |                             8.1 |                247.6% |
|          Linn |                   13.0 |                             5.7 |                164.9% |
|         Scott |                    1.1 |                             0.7 |               \-40.0% |
|       Johnson |                    4.4 |                             2.9 |                111.2% |
|    Black Hawk |                   20.9 |                            15.9 |                 62.8% |
|      Woodbury |                  \-1.6 |                           \-1.5 |              \-116.7% |
|       Dubuque |                    4.3 |                             4.4 |                 94.8% |
|         Story |                    6.6 |                             6.8 |                253.3% |
|        Dallas |                   11.3 |                            12.1 |                437.4% |
| Pottawattamie |                    1.9 |                             2.0 |                 11.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.6 |                           109.1 |              1 978.5% |
|    Decatur |                    3.4 |                            43.6 |                209.9% |
|    Fremont |                    2.7 |                            39.0 |                224.9% |
|      Henry |                    6.7 |                            33.6 |                391.0% |
|     Keokuk |                    3.4 |                            33.5 |                287.5% |
|     Monroe |                    2.6 |                            33.4 |                212.4% |
|   Franklin |                    2.7 |                            27.0 |                116.7% |
|     Monona |                    2.3 |                            26.5 |                228.6% |
| Montgomery |                    2.4 |                            24.5 |                200.0% |
|   Humboldt |                    2.3 |                            23.9 |                 35.3% |

Most growth in positive cases, week-over-week:

|  county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------: | ---------------------: | ------------------------------: | --------------------: |
|  Jasper |                   40.6 |                           109.1 |              1 978.5% |
|  Dallas |                   11.3 |                            12.1 |                437.4% |
|   Henry |                    6.7 |                            33.6 |                391.0% |
|  Keokuk |                    3.4 |                            33.5 |                287.5% |
|   Story |                    6.6 |                             6.8 |                253.3% |
|    Polk |                   39.7 |                             8.1 |                247.6% |
| Madison |                    2.9 |                            17.5 |                237.4% |
|  Monona |                    2.3 |                            26.5 |                228.6% |
| Fremont |                    2.7 |                            39.0 |                224.9% |
|  Monroe |                    2.6 |                            33.4 |                212.4% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.3 |                          \-20.3 |              \-277.8% |
|   Mahaska |                  \-3.1 |                          \-14.2 |              \-236.4% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Carroll |                  \-2.4 |                          \-12.0 |              \-200.0% |
|    Shelby |                  \-1.6 |                          \-13.7 |              \-144.4% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-128.6% |
|  Woodbury |                  \-1.6 |                           \-1.5 |              \-116.7% |
|     Mills |                  \-1.0 |                           \-6.6 |              \-100.0% |
|     Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
|     Worth |                  \-1.0 |                          \-13.5 |              \-100.0% |
