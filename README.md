Compiled at 2021-06-12 20:15:49 UTC

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

## Tables as of 2021-06-11

As of 2021-06-11, IPDH is reporting 80 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   13.1 |                             2.7 |                  5.3% |
|          Linn |                    9.4 |                             4.2 |                  5.8% |
|         Scott |                    3.4 |                             2.0 |               \-50.0% |
|       Johnson |                    1.6 |                             1.0 |               \-52.6% |
|    Black Hawk |                   10.6 |                             8.1 |                 30.6% |
|      Woodbury |                    2.1 |                             2.1 |                 22.2% |
|       Dubuque |                    2.7 |                             2.8 |               \-27.8% |
|         Story |                    1.1 |                             1.2 |               \-40.0% |
|        Dallas |                    2.1 |                             2.3 |               \-18.5% |
| Pottawattamie |                    2.3 |                             2.5 |               \-14.8% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                  8.3% |
| Black Hawk |                   10.6 |                             8.1 |                 30.6% |
|     Taylor |                    0.4 |                             7.0 |                 25.0% |
|       Page |                    1.0 |                             6.6 |                 27.3% |
|     Louisa |                    0.7 |                             6.5 |                 50.0% |
|   Ringgold |                    0.3 |                             5.8 |                 28.6% |
|      Union |                    0.7 |                             5.8 |                  9.1% |
|   Buchanan |                    1.1 |                             5.4 |                 66.6% |
|       Tama |                    0.9 |                             5.1 |                 85.7% |
|    Clayton |                    0.9 |                             4.9 |                 62.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Carroll |                    0.3 |                             1.4 |                125.2% |
|    Wapello |                    0.9 |                             2.5 |                 85.7% |
|       Tama |                    0.9 |                             5.1 |                 85.7% |
|   Harrison |                    0.4 |                             3.1 |                 66.7% |
|   Buchanan |                    1.1 |                             5.4 |                 66.6% |
|    Clayton |                    0.9 |                             4.9 |                 62.5% |
|     Warren |                    2.3 |                             4.4 |                 53.3% |
|     Louisa |                    0.7 |                             6.5 |                 50.0% |
|     Grundy |                    0.4 |                             3.5 |                 42.9% |
| Black Hawk |                   10.6 |                             8.1 |                 30.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Winneshiek |                  \-0.1 |                           \-0.7 |               \-53.9% |
|   Marshall |                    0.0 |                             0.0 |               \-53.3% |
|     Hardin |                    0.0 |                             0.0 |               \-53.3% |
|     Wright |                    0.0 |                             0.0 |               \-53.3% |
|    Johnson |                    1.6 |                             1.0 |               \-52.6% |
|      Scott |                    3.4 |                             2.0 |               \-50.0% |
| Des Moines |                    1.3 |                             3.3 |               \-46.7% |
|      Jones |                    0.0 |                             0.0 |               \-46.1% |
| Washington |                    0.6 |                             2.6 |               \-45.0% |
|      Davis |                    0.1 |                             1.6 |               \-42.8% |
