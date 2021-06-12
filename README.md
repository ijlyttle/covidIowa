Compiled at 2021-06-12 16:59:55 UTC

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

As of 2021-06-11, IPDH is reporting 207 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-11 |                   97.3 |                             3.1 |                \-3.0% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   16.9 |                             3.4 |                 33.0% |
|          Linn |                   10.9 |                             4.8 |                 20.3% |
|         Scott |                    4.3 |                             2.5 |               \-40.3% |
|       Johnson |                    2.9 |                             1.9 |               \-29.0% |
|    Black Hawk |                   13.4 |                            10.2 |                 62.9% |
|      Woodbury |                    2.6 |                             2.5 |                 38.9% |
|       Dubuque |                    3.1 |                             3.2 |               \-19.4% |
|         Story |                    1.1 |                             1.2 |               \-40.0% |
|        Dallas |                    3.0 |                             3.2 |                  3.7% |
| Pottawattamie |                    2.6 |                             2.8 |                \-7.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                  8.3% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
| Black Hawk |                   13.4 |                            10.2 |                 62.9% |
|     Louisa |                    0.9 |                             7.8 |                 62.5% |
|     Taylor |                    0.4 |                             7.0 |                 25.0% |
|   Hamilton |                    1.0 |                             6.8 |                 40.0% |
|       Page |                    1.0 |                             6.6 |                 27.3% |
|       Tama |                    1.0 |                             5.9 |                100.0% |
|      Union |                    0.7 |                             5.8 |                  9.1% |
|   Buchanan |                    1.1 |                             5.4 |                 66.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Carroll |                    0.3 |                             1.4 |                125.2% |
|    Wapello |                    1.0 |                             2.9 |                100.0% |
|       Tama |                    1.0 |                             5.9 |                100.0% |
|   Harrison |                    0.4 |                             3.1 |                 66.7% |
|   Buchanan |                    1.1 |                             5.4 |                 66.6% |
| Black Hawk |                   13.4 |                            10.2 |                 62.9% |
|    Clayton |                    0.9 |                             4.9 |                 62.5% |
|     Louisa |                    0.9 |                             7.8 |                 62.5% |
|     Warren |                    2.4 |                             4.7 |                 60.0% |
|     Jasper |                    0.6 |                             1.5 |                 57.1% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Wright |                  \-0.1 |                           \-1.1 |               \-60.0% |
|   Marshall |                    0.0 |                             0.0 |               \-53.3% |
| Washington |                    0.4 |                             2.0 |               \-50.0% |
| Des Moines |                    1.3 |                             3.3 |               \-46.7% |
|     Hardin |                    0.1 |                             0.8 |               \-46.7% |
|      Jones |                    0.0 |                             0.0 |               \-46.1% |
|      Scott |                    4.3 |                             2.5 |               \-40.3% |
|      Story |                    1.1 |                             1.2 |               \-40.0% |
|   Franklin |                    0.3 |                             2.8 |               \-40.0% |
|  Winnebago |                    0.3 |                             2.8 |               \-35.7% |
