Compiled at 2021-06-08 17:32:32 UTC

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

## Tables as of 2021-06-08

As of 2021-06-08, IPDH is reporting 69 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   16.1 |                             3.3 |                 14.3% |
|          Linn |                   13.0 |                             5.7 |                 69.0% |
|         Scott |                    5.4 |                             3.1 |               \-36.6% |
|       Johnson |                    3.4 |                             2.3 |               \-20.5% |
|    Black Hawk |                   10.9 |                             8.3 |                 76.6% |
|      Woodbury |                    2.0 |                             1.9 |               \-22.2% |
|       Dubuque |                    4.4 |                             4.6 |                  5.6% |
|         Story |                    1.6 |                             1.6 |               \-37.9% |
|        Dallas |                    3.6 |                             3.8 |                 52.4% |
| Pottawattamie |                    3.7 |                             4.0 |                153.9% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    1.6 |                            28.6 |                124.9% |
|   Franklin |                    1.0 |                             9.9 |                 40.0% |
|      Emmet |                    0.9 |                             9.3 |                 18.2% |
|  Winnebago |                    0.9 |                             8.3 |                \-7.2% |
| Black Hawk |                   10.9 |                             8.3 |                 76.6% |
|      Union |                    1.0 |                             8.2 |                 27.3% |
|        Lee |                    2.6 |                             7.6 |                 47.0% |
| Washington |                    1.6 |                             7.2 |                 99.9% |
| Des Moines |                    2.7 |                             7.0 |                  8.3% |
|     Bremer |                    1.6 |                             6.3 |                 50.0% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
| Pottawattamie |                    3.7 |                             4.0 |                153.9% |
|       Audubon |                    1.6 |                            28.6 |                124.9% |
|        Hardin |                    0.9 |                             5.1 |                116.7% |
|    Washington |                    1.6 |                             7.2 |                 99.9% |
|     Allamakee |                    0.6 |                             4.2 |                 83.3% |
|    Black Hawk |                   10.9 |                             8.3 |                 76.6% |
|          Linn |                   13.0 |                             5.7 |                 69.0% |
|       Fayette |                    0.9 |                             4.4 |                 62.5% |
|        Wright |                    0.6 |                             4.5 |                 57.1% |
|        Dallas |                    3.6 |                             3.8 |                 52.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Jones |                    0.0 |                             0.0 |               \-63.2% |
| Cerro Gordo |                    2.0 |                             4.7 |               \-47.5% |
|    Marshall |                    0.3 |                             0.7 |               \-47.1% |
|   Poweshiek |                    0.3 |                             1.5 |               \-43.7% |
|        Iowa |                    0.0 |                             0.0 |               \-41.7% |
|       Davis |                    0.3 |                             3.2 |               \-40.0% |
|       Story |                    1.6 |                             1.6 |               \-37.9% |
|       Scott |                    5.4 |                             3.1 |               \-36.6% |
|     Carroll |                  \-0.1 |                           \-0.7 |               \-33.4% |
|       Boone |                    0.6 |                             2.2 |               \-31.3% |
