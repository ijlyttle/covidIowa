Compiled at 2021-06-07 18:27:50 UTC

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

## Tables as of 2021-06-07

As of 2021-06-07, IPDH is reporting 40 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   13.3 |                             2.7 |                \-6.5% |
|          Linn |                   12.3 |                             5.4 |                 55.0% |
|         Scott |                    5.4 |                             3.1 |               \-40.8% |
|       Johnson |                    3.4 |                             2.3 |               \-27.9% |
|    Black Hawk |                    9.0 |                             6.9 |                 40.0% |
|      Woodbury |                    1.9 |                             1.8 |               \-28.6% |
|       Dubuque |                    4.3 |                             4.4 |               \-15.9% |
|         Story |                    1.6 |                             1.6 |               \-35.7% |
|        Dallas |                    3.3 |                             3.5 |                 36.4% |
| Pottawattamie |                    3.4 |                             3.7 |                121.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                 62.5% |
|   Franklin |                    1.0 |                             9.9 |                 40.0% |
|  Winnebago |                    0.9 |                             8.3 |                \-7.2% |
|      Union |                    1.0 |                             8.2 |                 27.3% |
| Washington |                    1.7 |                             7.8 |                 72.8% |
| Black Hawk |                    9.0 |                             6.9 |                 40.0% |
|        Lee |                    2.3 |                             6.8 |                  9.5% |
|        Ida |                    0.4 |                             6.3 |               \-16.6% |
| Des Moines |                    2.4 |                             6.2 |                \-4.0% |
|      Emmet |                    0.6 |                             6.2 |               \-21.5% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
| Pottawattamie |                    3.4 |                             3.7 |                121.4% |
|        Hardin |                    0.9 |                             5.1 |                 85.7% |
|    Washington |                    1.7 |                             7.8 |                 72.8% |
|       Fayette |                    0.9 |                             4.4 |                 62.5% |
|       Audubon |                    0.9 |                            15.6 |                 62.5% |
|     Allamakee |                    0.6 |                             4.2 |                 57.1% |
|        Wright |                    0.6 |                             4.5 |                 57.1% |
|          Linn |                   12.3 |                             5.4 |                 55.0% |
|    Black Hawk |                    9.0 |                             6.9 |                 40.0% |
|      Franklin |                    1.0 |                             9.9 |                 40.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Jones |                    0.0 |                             0.0 |               \-63.2% |
| Cerro Gordo |                    1.9 |                             4.4 |               \-50.0% |
|      Shelby |                  \-0.3 |                           \-2.5 |               \-44.5% |
|   Poweshiek |                    0.3 |                             1.5 |               \-43.7% |
|        Iowa |                    0.0 |                             0.0 |               \-41.7% |
|    Marshall |                    0.4 |                             1.1 |               \-41.2% |
|       Scott |                    5.4 |                             3.1 |               \-40.8% |
|       Davis |                    0.3 |                             3.2 |               \-40.0% |
|    Delaware |                    0.0 |                             0.0 |               \-36.3% |
|       Story |                    1.6 |                             1.6 |               \-35.7% |
