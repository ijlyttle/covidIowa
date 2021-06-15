Compiled at 2021-06-15 17:04:52 UTC

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

## Tables as of 2021-06-15

As of 2021-06-15, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    9.9 |                             2.0 |               \-36.7% |
|          Linn |                    6.9 |                             3.0 |               \-43.9% |
|         Scott |                    2.9 |                             1.7 |               \-40.0% |
|       Johnson |                    2.4 |                             1.6 |               \-22.6% |
|    Black Hawk |                   11.9 |                             9.0 |                  8.4% |
|      Woodbury |                    2.1 |                             2.1 |                  4.8% |
|       Dubuque |                    3.0 |                             3.1 |               \-26.3% |
|         Story |                    1.0 |                             1.0 |               \-22.2% |
|        Dallas |                    1.9 |                             2.0 |               \-37.5% |
| Pottawattamie |                    2.3 |                             2.5 |               \-30.3% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Ringgold |                    0.6 |                            11.7 |                 57.1% |
|  Black Hawk |                   11.9 |                             9.0 |                  8.4% |
|      Taylor |                    0.4 |                             7.0 |                 42.9% |
| Cerro Gordo |                    2.7 |                             6.4 |                 23.8% |
|        Page |                    0.9 |                             5.7 |                  8.3% |
|       Cedar |                    1.0 |                             5.4 |                 55.5% |
|     Audubon |                    0.3 |                             5.2 |               \-50.0% |
|      Shelby |                    0.6 |                             5.0 |                 83.3% |
|    Hamilton |                    0.7 |                             4.8 |                 19.9% |
|     Webster |                    1.7 |                             4.8 |                 58.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Shelby |                    0.6 |                             5.0 |                 83.3% |
|    Webster |                    1.7 |                             4.8 |                 58.3% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
|   Buchanan |                    1.0 |                             4.7 |                 55.5% |
|      Cedar |                    1.0 |                             5.4 |                 55.5% |
|     Taylor |                    0.4 |                             7.0 |                 42.9% |
|      Mills |                    0.6 |                             3.8 |                 37.4% |
| Winneshiek |                    0.7 |                             3.6 |                 33.3% |
|  Jefferson |                    0.3 |                             1.6 |                 28.6% |
|     Jasper |                    0.4 |                             1.2 |                 25.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Bremer |                    0.0 |                             0.0 |               \-61.1% |
|  Des Moines |                    0.6 |                             1.5 |               \-57.7% |
| Buena Vista |                  \-0.1 |                           \-0.7 |               \-50.0% |
|     Audubon |                    0.3 |                             5.2 |               \-50.0% |
|     Madison |                    0.0 |                             0.0 |               \-46.1% |
|       Emmet |                    0.0 |                             0.0 |               \-46.1% |
|        Linn |                    6.9 |                             3.0 |               \-43.9% |
|       Union |                    0.1 |                             1.2 |               \-42.8% |
|    Franklin |                    0.1 |                             1.4 |               \-42.8% |
|    Crawford |                    0.0 |                             0.0 |               \-41.7% |
