Compiled at 2021-06-10 20:16:14 UTC

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

## Tables as of 2021-06-10

As of 2021-06-10, IPDH is reporting 70 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   15.0 |                             3.1 |                 27.3% |
|          Linn |                    9.4 |                             4.2 |                  5.8% |
|         Scott |                    3.0 |                             1.7 |               \-60.0% |
|       Johnson |                    3.0 |                             2.0 |               \-15.1% |
|    Black Hawk |                   10.3 |                             7.8 |                 31.7% |
|      Woodbury |                    1.4 |                             1.4 |               \-34.6% |
|       Dubuque |                    2.6 |                             2.6 |               \-21.9% |
|         Story |                    1.6 |                             1.6 |               \-28.0% |
|        Dallas |                    2.4 |                             2.6 |                \-4.0% |
| Pottawattamie |                    2.4 |                             2.6 |                  0.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                 18.2% |
|   Franklin |                    0.9 |                             8.5 |                 18.2% |
| Black Hawk |                   10.3 |                             7.8 |                 31.7% |
|       Page |                    1.0 |                             6.6 |                 27.3% |
|      Emmet |                    0.6 |                             6.2 |               \-15.4% |
|   Ringgold |                    0.3 |                             5.8 |                 28.6% |
|      Union |                    0.7 |                             5.8 |                  9.1% |
|        Lee |                    1.9 |                             5.5 |                  5.3% |
|     Louisa |                    0.6 |                             5.2 |                  9.9% |
|     Warren |                    2.6 |                             5.0 |                 47.0% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  O’Brien |                    0.0 |                             0.0 |                 75.1% |
|     Tama |                    0.7 |                             4.2 |                 71.4% |
|   Shelby |                    0.6 |                             5.0 |                 57.1% |
|  Carroll |                    0.3 |                             1.4 |                 50.1% |
|  Clayton |                    0.7 |                             4.1 |                 50.0% |
|   Warren |                    2.6 |                             5.0 |                 47.0% |
| Harrison |                    0.4 |                             3.1 |                 42.9% |
|   Grundy |                    0.4 |                             3.5 |                 42.9% |
|   Howard |                    0.4 |                             4.7 |                 42.9% |
|    Cedar |                    0.6 |                             3.1 |                 37.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Scott |                    3.0 |                             1.7 |               \-60.0% |
|   Crawford |                  \-0.1 |                           \-0.8 |               \-50.0% |
|  Muscatine |                    1.0 |                             2.3 |               \-48.1% |
|      Jones |                    0.0 |                             0.0 |               \-46.1% |
|  Van Buren |                  \-0.1 |                           \-2.0 |               \-45.4% |
| Washington |                    0.3 |                             1.3 |               \-43.7% |
|   Marshall |                    0.1 |                             0.4 |               \-42.8% |
|      Davis |                    0.1 |                             1.6 |               \-42.8% |
|     Clarke |                    0.0 |                             0.0 |               \-36.3% |
|        Ida |                    0.0 |                             0.0 |               \-36.3% |
