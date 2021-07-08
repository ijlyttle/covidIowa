Compiled at 2021-07-08 20:19:07 UTC

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

## Tables as of 2021-07-08

As of 2021-07-08, IPDH is reporting 139 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   38.1 |                             7.8 |                356.7% |
|          Linn |                   10.3 |                             4.5 |                 97.5% |
|         Scott |                    1.3 |                             0.7 |               \-38.4% |
|       Johnson |                    3.9 |                             2.6 |                 25.9% |
|    Black Hawk |                   18.1 |                            13.8 |                 25.2% |
|      Woodbury |                  \-2.1 |                           \-2.1 |              \-144.5% |
|       Dubuque |                    4.0 |                             4.1 |                 66.7% |
|         Story |                    6.6 |                             6.8 |                231.2% |
|        Dallas |                   10.0 |                            10.7 |                450.0% |
| Pottawattamie |                    1.0 |                             1.1 |               \-12.5% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.9 |                           109.9 |              2 154.0% |
|    Decatur |                    3.3 |                            41.8 |                172.8% |
|    Fremont |                    2.7 |                            39.0 |                271.4% |
|      Henry |                    7.3 |                            36.5 |                624.9% |
|   Franklin |                    2.7 |                            27.0 |                188.8% |
|   Humboldt |                    2.6 |                            26.9 |                 66.6% |
|     Monroe |                    2.0 |                            26.0 |                162.5% |
|      Wayne |                    1.6 |                            24.4 |                 50.0% |
|     Keokuk |                    2.4 |                            23.7 |                140.0% |
| Montgomery |                    2.1 |                            21.6 |                214.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.9 |                           109.9 |              2 154.0% |
|      Henry |                    7.3 |                            36.5 |                624.9% |
|     Dallas |                   10.0 |                            10.7 |                450.0% |
|       Polk |                   38.1 |                             7.8 |                356.7% |
|    Fremont |                    2.7 |                            39.0 |                271.4% |
|      Story |                    6.6 |                             6.8 |                231.2% |
| Montgomery |                    2.1 |                            21.6 |                214.3% |
|     Warren |                    6.3 |                            12.2 |                200.0% |
|    Madison |                    2.0 |                            12.2 |                200.0% |
|     Monona |                    1.6 |                            18.2 |                200.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.0 |                          \-18.5 |              \-275.0% |
|   Mahaska |                  \-2.9 |                          \-12.9 |              \-262.5% |
|   Carroll |                  \-2.6 |                          \-12.8 |              \-222.2% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-212.5% |
|  Woodbury |                  \-2.1 |                           \-2.1 |              \-144.5% |
|    Shelby |                  \-1.6 |                          \-13.7 |              \-144.4% |
|    Marion |                  \-1.4 |                           \-4.3 |              \-137.5% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-125.0% |
|     Union |                  \-1.1 |                           \-9.3 |              \-114.3% |
|     Worth |                  \-1.1 |                          \-15.5 |              \-112.5% |
