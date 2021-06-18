Compiled at 2021-06-18 17:12:15 UTC

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

## Tables as of 2021-06-18

As of 2021-06-18, IPDH is reporting 70 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.7 |                             2.4 |               \-10.1% |
|          Linn |                    7.3 |                             3.2 |               \-20.5% |
|         Scott |                    3.6 |                             2.1 |                  3.2% |
|       Johnson |                    2.7 |                             1.8 |                 44.5% |
|    Black Hawk |                   13.3 |                            10.1 |                 23.5% |
|      Woodbury |                    2.0 |                             1.9 |                \-4.5% |
|       Dubuque |                    2.6 |                             2.6 |                \-3.9% |
|         Story |                    1.0 |                             1.0 |                \-6.7% |
|        Dallas |                    1.6 |                             1.7 |               \-18.2% |
| Pottawattamie |                    2.0 |                             2.1 |                \-8.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.9 |                            15.6 |                  0.0% |
|  Black Hawk |                   13.3 |                            10.1 |                 23.5% |
|  Winneshiek |                    1.9 |                             9.3 |                233.4% |
|    Ringgold |                    0.4 |                             8.8 |                 11.1% |
|       Mills |                    1.1 |                             7.6 |                 66.6% |
|      Benton |                    1.9 |                             7.2 |                 81.9% |
|    Crawford |                    1.1 |                             6.8 |                150.1% |
| Cerro Gordo |                    2.9 |                             6.7 |                 35.0% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|       Worth |                    0.4 |                             5.8 |                 42.9% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Winneshiek |                    1.9 |                             9.3 |                233.4% |
|    Crawford |                    1.1 |                             6.8 |                150.1% |
|      Benton |                    1.9 |                             7.2 |                 81.9% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|       Mills |                    1.1 |                             7.6 |                 66.6% |
|    Marshall |                    0.6 |                             1.4 |                 57.1% |
|         Ida |                    0.3 |                             4.2 |                 50.1% |
|     Johnson |                    2.7 |                             1.8 |                 44.5% |
|      Jasper |                    0.9 |                             2.3 |                 44.4% |
|      Hardin |                    0.4 |                             2.5 |                 42.9% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Clinton |                    0.1 |                             0.3 |               \-50.0% |
|     Page |                    0.0 |                             0.0 |               \-50.0% |
|    Emmet |                  \-0.1 |                           \-1.6 |               \-40.0% |
|  Clayton |                    0.1 |                             0.8 |               \-38.4% |
|   Warren |                    1.1 |                             2.2 |               \-34.8% |
|   Howard |                  \-0.1 |                           \-1.6 |               \-33.4% |
|   Marion |                    0.1 |                             0.4 |               \-33.3% |
|    Union |                    0.1 |                             1.2 |               \-33.3% |
|   Louisa |                    0.1 |                             1.3 |               \-33.3% |
| Harrison |                    0.0 |                             0.0 |               \-30.0% |
