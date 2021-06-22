Compiled at 2021-06-22 17:31:22 UTC

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

## Tables as of 2021-06-22

As of 2021-06-22, IPDH is reporting 70 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.4 |                             2.3 |                 14.5% |
|          Linn |                    7.1 |                             3.2 |                  3.6% |
|         Scott |                    2.9 |                             1.7 |                  0.0% |
|       Johnson |                    1.7 |                             1.1 |               \-20.9% |
|    Black Hawk |                   15.0 |                            11.4 |                 24.4% |
|      Woodbury |                    1.6 |                             1.5 |               \-18.2% |
|       Dubuque |                    2.6 |                             2.6 |               \-10.7% |
|         Story |                    1.4 |                             1.5 |                 21.5% |
|        Dallas |                    1.3 |                             1.4 |               \-20.0% |
| Pottawattamie |                    2.0 |                             2.1 |                \-8.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.9 |                            15.6 |                 44.4% |
|  Black Hawk |                   15.0 |                            11.4 |                 24.4% |
|      Keokuk |                    1.0 |                             9.8 |                100.0% |
|      Benton |                    2.1 |                             8.4 |                 83.4% |
| Buena Vista |                    1.6 |                             8.0 |                200.0% |
|    Buchanan |                    1.4 |                             6.7 |                 21.5% |
|  Winneshiek |                    1.3 |                             6.4 |                 33.4% |
|       Worth |                    0.4 |                             5.8 |                 11.1% |
|      Bremer |                    1.4 |                             5.7 |                142.9% |
|       Mills |                    0.9 |                             5.7 |                 18.2% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    1.6 |                             8.0 |                200.0% |
|      Bremer |                    1.4 |                             5.7 |                142.9% |
|       Henry |                    0.7 |                             3.6 |                100.0% |
|      Keokuk |                    1.0 |                             9.8 |                100.0% |
|      Benton |                    2.1 |                             8.4 |                 83.4% |
|     Carroll |                    0.6 |                             2.8 |                 83.3% |
|    Crawford |                    0.7 |                             4.2 |                 71.4% |
|     Mahaska |                    0.7 |                             3.2 |                 50.0% |
|      Butler |                    0.7 |                             4.9 |                 50.0% |
|    Marshall |                    0.9 |                             2.2 |                 44.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Warren |                    0.0 |                             0.0 |               \-68.2% |
|        Page |                    0.0 |                             0.0 |               \-46.1% |
| Cerro Gordo |                    1.1 |                             2.7 |               \-42.3% |
|      Shelby |                    0.0 |                             0.0 |               \-36.3% |
|       Cedar |                    0.3 |                             1.5 |               \-35.7% |
|         Ida |                  \-0.1 |                           \-2.1 |               \-33.4% |
|         Lee |                    0.7 |                             2.1 |               \-29.4% |
|      Marion |                    0.1 |                             0.4 |               \-27.2% |
|    Ringgold |                    0.1 |                             2.9 |               \-27.2% |
|     Clinton |                    0.3 |                             0.6 |               \-25.0% |
