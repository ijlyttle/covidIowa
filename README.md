Compiled at 2021-07-10 20:27:50 UTC

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

## Tables as of 2021-07-10

As of 2021-07-10, IPDH is reporting 143 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   39.0 |                             8.0 |                245.7% |
|          Linn |                   11.9 |                             5.2 |                109.3% |
|         Scott |                    0.7 |                             0.4 |               \-57.2% |
|       Johnson |                    4.1 |                             2.7 |                 80.0% |
|    Black Hawk |                   20.1 |                            15.3 |                 55.8% |
|      Woodbury |                  \-1.6 |                           \-1.5 |              \-118.2% |
|       Dubuque |                    4.1 |                             4.3 |                 56.5% |
|         Story |                    6.6 |                             6.8 |                278.5% |
|        Dallas |                   10.9 |                            11.6 |                453.3% |
| Pottawattamie |                    1.4 |                             1.5 |               \-10.5% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.7 |                           109.5 |              1 985.7% |
|    Decatur |                    3.1 |                            39.9 |                123.1% |
|    Fremont |                    2.7 |                            39.0 |                224.9% |
|      Henry |                    7.0 |                            35.1 |                459.8% |
|     Keokuk |                    3.3 |                            32.1 |                233.3% |
|     Monroe |                    2.3 |                            29.7 |                228.6% |
|   Franklin |                    2.6 |                            25.5 |                108.3% |
| Montgomery |                    2.4 |                            24.5 |                242.9% |
|   Humboldt |                    2.3 |                            23.9 |                 35.3% |
|     Monona |                    2.0 |                            23.2 |                200.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.7 |                           109.5 |              1 985.7% |
|      Henry |                    7.0 |                            35.1 |                459.8% |
|     Dallas |                   10.9 |                            11.6 |                453.3% |
|      Story |                    6.6 |                             6.8 |                278.5% |
|       Polk |                   39.0 |                             8.0 |                245.7% |
| Montgomery |                    2.4 |                            24.5 |                242.9% |
|     Keokuk |                    3.3 |                            32.1 |                233.3% |
|     Monroe |                    2.3 |                            29.7 |                228.6% |
|    Fremont |                    2.7 |                            39.0 |                224.9% |
|  Allamakee |                    2.6 |                            18.8 |                212.4% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.0 |                          \-18.5 |              \-300.0% |
|   Mahaska |                  \-3.0 |                          \-13.6 |              \-275.0% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Carroll |                  \-2.4 |                          \-12.0 |              \-200.0% |
|    Shelby |                  \-1.9 |                          \-16.2 |              \-175.0% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-125.0% |
|  Woodbury |                  \-1.6 |                           \-1.5 |              \-118.2% |
|     Worth |                  \-1.1 |                          \-15.5 |              \-112.5% |
|     Mills |                  \-1.0 |                           \-6.6 |              \-100.0% |
|     Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
