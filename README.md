Compiled at 2021-06-19 20:15:44 UTC

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

## Tables as of 2021-06-19

As of 2021-06-19, IPDH is reporting 79 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   10.9 |                             2.2 |               \-24.5% |
|          Linn |                    7.1 |                             3.2 |               \-12.3% |
|         Scott |                    3.1 |                             1.8 |                \-3.3% |
|       Johnson |                    1.7 |                             1.1 |               \-26.9% |
|    Black Hawk |                   12.3 |                             9.4 |                  4.5% |
|      Woodbury |                    1.7 |                             1.7 |               \-17.4% |
|       Dubuque |                    2.3 |                             2.3 |               \-17.8% |
|         Story |                    1.1 |                             1.2 |                \-6.3% |
|        Dallas |                    0.6 |                             0.6 |               \-54.2% |
| Pottawattamie |                    1.9 |                             2.0 |               \-16.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |               \-14.3% |
|  Black Hawk |                   12.3 |                             9.4 |                  4.5% |
|      Benton |                    2.0 |                             7.8 |                109.9% |
| Cerro Gordo |                    2.9 |                             6.7 |                 50.0% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|  Winneshiek |                    1.3 |                             6.4 |                 77.8% |
|      Keokuk |                    0.6 |                             5.6 |                 57.1% |
|       Floyd |                    0.9 |                             5.5 |                 18.2% |
|    Buchanan |                    1.1 |                             5.4 |                  7.2% |
|     Hancock |                    0.6 |                             5.4 |                 37.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Henry |                    1.0 |                             5.0 |                180.1% |
|      Benton |                    2.0 |                             7.8 |                109.9% |
|  Winneshiek |                    1.3 |                             6.4 |                 77.8% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|    Crawford |                    0.4 |                             2.6 |                 66.7% |
|    Marshall |                    0.6 |                             1.4 |                 57.1% |
|      Butler |                    0.6 |                             4.0 |                 57.1% |
|      Keokuk |                    0.6 |                             5.6 |                 57.1% |
| Cerro Gordo |                    2.9 |                             6.7 |                 50.0% |
|     Carroll |                    0.6 |                             2.8 |                 37.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Dallas |                    0.6 |                             0.6 |               \-54.2% |
|       Page |                    0.0 |                             0.0 |               \-50.0% |
|    Clayton |                    0.0 |                             0.0 |               \-36.3% |
|     Louisa |                    0.0 |                             0.0 |               \-36.3% |
|   Hamilton |                    0.3 |                             1.9 |               \-35.7% |
|     Howard |                  \-0.1 |                           \-1.6 |               \-33.4% |
|     Warren |                    1.0 |                             1.9 |               \-33.3% |
| Washington |                    0.1 |                             0.7 |               \-33.3% |
|    Clinton |                    0.3 |                             0.6 |               \-30.7% |
|    Jackson |                    0.0 |                             0.0 |               \-30.0% |
