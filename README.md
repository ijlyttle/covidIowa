Compiled at 2021-06-17 20:15:46 UTC

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

## Tables as of 2021-06-17

As of 2021-06-17, IPDH is reporting 74 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.4 |                             2.3 |               \-22.3% |
|          Linn |                    7.7 |                             3.4 |               \-16.4% |
|         Scott |                    3.9 |                             2.2 |                 21.4% |
|       Johnson |                    2.9 |                             1.9 |                \-3.6% |
|    Black Hawk |                   13.4 |                            10.2 |                 27.8% |
|      Woodbury |                    2.7 |                             2.6 |                 52.9% |
|       Dubuque |                    3.3 |                             3.4 |                 20.0% |
|         Story |                    1.1 |                             1.2 |               \-16.6% |
|        Dallas |                    1.9 |                             2.0 |               \-16.7% |
| Pottawattamie |                    2.3 |                             2.5 |                \-4.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    1.3 |                            23.4 |                 23.1% |
|  Black Hawk |                   13.4 |                            10.2 |                 27.8% |
|       Mills |                    1.1 |                             7.6 |                 87.5% |
|  Winneshiek |                    1.3 |                             6.4 |                100.0% |
| Cerro Gordo |                    2.6 |                             6.1 |                 25.0% |
|    Ringgold |                    0.3 |                             5.8 |                  0.0% |
| Buena Vista |                    1.1 |                             5.8 |                 50.0% |
|      Monroe |                    0.4 |                             5.6 |                 11.1% |
|     Decatur |                    0.4 |                             5.5 |                 42.9% |
|    Buchanan |                    1.1 |                             5.4 |                 25.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Winneshiek |                    1.3 |                             6.4 |                100.0% |
|    Crawford |                    0.7 |                             4.2 |                100.0% |
|       Mills |                    1.1 |                             7.6 |                 87.5% |
|    Woodbury |                    2.7 |                             2.6 |                 52.9% |
|       Henry |                    0.7 |                             3.6 |                 50.0% |
| Buena Vista |                    1.1 |                             5.8 |                 50.0% |
|      Butler |                    0.4 |                             3.0 |                 42.9% |
|   Chickasaw |                    0.4 |                             3.6 |                 42.9% |
|     Decatur |                    0.4 |                             5.5 |                 42.9% |
|      Jasper |                    0.6 |                             1.5 |                 37.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    0.0 |                             0.0 |               \-50.0% |
|     Warren |                    1.0 |                             1.9 |               \-44.0% |
|    Clayton |                    0.0 |                             0.0 |               \-41.7% |
|    Clinton |                    0.4 |                             0.9 |               \-41.2% |
|   Harrison |                  \-0.1 |                           \-1.0 |               \-40.0% |
|     Howard |                  \-0.1 |                           \-1.6 |               \-40.0% |
|   Franklin |                    0.1 |                             1.4 |               \-38.4% |
| Des Moines |                    0.7 |                             1.8 |               \-36.8% |
|     Shelby |                    0.0 |                             0.0 |               \-36.3% |
|      Emmet |                    0.0 |                             0.0 |               \-36.3% |
