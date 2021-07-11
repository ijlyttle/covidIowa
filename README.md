Compiled at 2021-07-11 20:15:43 UTC

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

## Tables as of 2021-07-11

As of 2021-07-11, IPDH is reporting 86 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   39.6 |                             8.1 |                259.5% |
|          Linn |                   12.7 |                             5.6 |                146.2% |
|         Scott |                    1.1 |                             0.7 |               \-48.3% |
|       Johnson |                    4.4 |                             2.9 |                111.2% |
|    Black Hawk |                   19.7 |                            15.0 |                 48.0% |
|      Woodbury |                  \-1.9 |                           \-1.8 |              \-126.1% |
|       Dubuque |                    4.3 |                             4.4 |                 76.2% |
|         Story |                    6.6 |                             6.8 |                278.5% |
|        Dallas |                   11.1 |                            11.9 |                431.2% |
| Pottawattamie |                    1.7 |                             1.8 |                \-9.5% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.7 |                           109.5 |              2 146.3% |
|    Decatur |                    3.4 |                            43.6 |                158.4% |
|    Fremont |                    2.7 |                            39.0 |                224.9% |
|      Henry |                    6.7 |                            33.6 |                315.4% |
|     Keokuk |                    3.3 |                            32.1 |                328.6% |
|     Monroe |                    2.3 |                            29.7 |                228.6% |
|     Monona |                    2.3 |                            26.5 |                228.6% |
| Montgomery |                    2.6 |                            25.9 |                257.1% |
|   Franklin |                    2.6 |                            25.5 |                108.3% |
|   Humboldt |                    2.3 |                            23.9 |                 35.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.7 |                           109.5 |              2 146.3% |
|     Dallas |                   11.1 |                            11.9 |                431.2% |
|     Keokuk |                    3.3 |                            32.1 |                328.6% |
|      Henry |                    6.7 |                            33.6 |                315.4% |
|      Story |                    6.6 |                             6.8 |                278.5% |
|       Polk |                   39.6 |                             8.1 |                259.5% |
| Montgomery |                    2.6 |                            25.9 |                257.1% |
|    Madison |                    2.9 |                            17.5 |                237.4% |
|     Monona |                    2.3 |                            26.5 |                228.6% |
|     Monroe |                    2.3 |                            29.7 |                228.6% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.3 |                          \-20.3 |              \-277.8% |
|   Mahaska |                  \-3.3 |                          \-14.9 |              \-260.0% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Carroll |                  \-2.4 |                          \-12.0 |              \-200.0% |
|    Shelby |                  \-1.7 |                          \-15.0 |              \-155.5% |
|  Woodbury |                  \-1.9 |                           \-1.8 |              \-126.1% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-125.0% |
|     Mills |                  \-1.0 |                           \-6.6 |              \-100.0% |
|     Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
|     Worth |                  \-1.0 |                          \-13.5 |              \-100.0% |
