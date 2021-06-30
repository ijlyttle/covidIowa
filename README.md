Compiled at 2021-06-30 23:54:19 UTC

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

## Tables as of 2021-06-30

As of 2021-06-30, IPDH is reporting 117 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    7.9 |                             1.6 |                \-6.1% |
|          Linn |                    4.4 |                             2.0 |               \-29.6% |
|         Scott |                    2.7 |                             1.6 |                 44.5% |
|       Johnson |                    2.0 |                             1.3 |                \-4.5% |
|    Black Hawk |                   13.6 |                            10.3 |                  4.1% |
|      Woodbury |                    1.6 |                             1.5 |                 50.0% |
|       Dubuque |                    2.6 |                             2.6 |                 25.0% |
|         Story |                    1.3 |                             1.3 |                  6.7% |
|        Dallas |                    1.3 |                             1.4 |                 33.4% |
| Pottawattamie |                    1.0 |                             1.1 |               \-30.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    4.4 |                            12.3 |                100.0% |
|      Adams |                    0.4 |                            11.9 |                 25.0% |
| Winneshiek |                    2.1 |                            10.7 |                 69.3% |
|   Humboldt |                    1.0 |                            10.5 |                 75.0% |
| Black Hawk |                   13.6 |                            10.3 |                  4.1% |
|      Wayne |                    0.6 |                             8.9 |                 57.1% |
|       Lyon |                    1.0 |                             8.5 |                 27.3% |
|    Decatur |                    0.6 |                             7.3 |                 37.4% |
|     Hardin |                    1.1 |                             6.8 |                 66.6% |
|        Lee |                    2.1 |                             6.4 |                 83.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    4.4 |                            12.3 |                100.0% |
|        Lee |                    2.1 |                             6.4 |                 83.4% |
|   Humboldt |                    1.0 |                            10.5 |                 75.0% |
| Winneshiek |                    2.1 |                            10.7 |                 69.3% |
|     Hardin |                    1.1 |                             6.8 |                 66.6% |
|      Wayne |                    0.6 |                             8.9 |                 57.1% |
|  Dickinson |                    0.3 |                             1.7 |                 50.1% |
|   Woodbury |                    1.6 |                             1.5 |                 50.0% |
|     Warren |                    1.1 |                             2.2 |                 50.0% |
|      Scott |                    2.7 |                             1.6 |                 44.5% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|      Marshall |                    0.6 |                             1.4 |               \-50.0% |
|         Sioux |                    0.1 |                             0.4 |               \-42.8% |
|      Buchanan |                    0.1 |                             0.7 |               \-42.8% |
|        Keokuk |                    0.1 |                             1.4 |               \-42.8% |
|         Cedar |                  \-0.1 |                           \-0.8 |               \-40.0% |
|         Boone |                  \-0.1 |                           \-0.5 |               \-33.4% |
|       Audubon |                  \-0.1 |                           \-2.6 |               \-33.4% |
| Pottawattamie |                    1.0 |                             1.1 |               \-30.0% |
|         Jones |                    0.0 |                             0.0 |               \-30.0% |
|     Allamakee |                    0.0 |                             0.0 |               \-30.0% |
