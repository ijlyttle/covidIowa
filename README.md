Compiled at 2021-06-20 17:15:22 UTC

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

## Tables as of 2021-06-20

As of 2021-06-20, IPDH is reporting 57 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.4 |                             2.3 |                \-9.4% |
|          Linn |                    5.9 |                             2.6 |               \-23.8% |
|         Scott |                    3.1 |                             1.8 |                 20.8% |
|       Johnson |                    2.4 |                             1.6 |                  9.1% |
|    Black Hawk |                   13.3 |                            10.1 |                  3.1% |
|      Woodbury |                    1.9 |                             1.8 |                  5.3% |
|       Dubuque |                    2.0 |                             2.1 |               \-25.0% |
|         Story |                    1.0 |                             1.0 |                \-6.7% |
|        Dallas |                    0.7 |                             0.8 |               \-40.0% |
| Pottawattamie |                    2.0 |                             2.1 |                \-4.5% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    1.0 |                            18.2 |                 16.7% |
|  Black Hawk |                   13.3 |                            10.1 |                  3.1% |
|  Winneshiek |                    1.6 |                             7.9 |                 79.9% |
|    Buchanan |                    1.4 |                             6.7 |                 21.5% |
|      Benton |                    1.7 |                             6.7 |                 72.8% |
| Buena Vista |                    1.1 |                             5.8 |                 87.5% |
|      Monroe |                    0.4 |                             5.6 |                 25.0% |
|    Crawford |                    0.9 |                             5.1 |                 62.5% |
|   Chickasaw |                    0.6 |                             4.8 |                 37.4% |
|       Mills |                    0.7 |                             4.7 |                  9.1% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     O’Brien |                    0.1 |                             1.0 |                100.2% |
|    Marshall |                    1.0 |                             2.5 |                100.0% |
| Buena Vista |                    1.1 |                             5.8 |                 87.5% |
|       Henry |                    0.6 |                             2.9 |                 83.3% |
|  Winneshiek |                    1.6 |                             7.9 |                 79.9% |
|      Benton |                    1.7 |                             6.7 |                 72.8% |
|      Keokuk |                    0.4 |                             4.2 |                 66.7% |
|    Crawford |                    0.9 |                             5.1 |                 62.5% |
|      Butler |                    0.6 |                             4.0 |                 57.1% |
|     Madison |                    0.3 |                             1.8 |                 50.1% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Warren |                    0.3 |                             0.6 |               \-59.1% |
| Cerro Gordo |                    1.1 |                             2.7 |               \-46.4% |
|        Page |                    0.0 |                             0.0 |               \-46.1% |
|      Shelby |                    0.0 |                             0.0 |               \-46.1% |
|      Dallas |                    0.7 |                             0.8 |               \-40.0% |
|       Emmet |                  \-0.1 |                           \-1.6 |               \-40.0% |
|    Hamilton |                    0.3 |                             1.9 |               \-30.7% |
|      Marion |                    0.1 |                             0.4 |               \-27.2% |
|  Washington |                    0.1 |                             0.7 |               \-27.2% |
|       Union |                    0.1 |                             1.2 |               \-27.2% |
