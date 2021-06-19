Compiled at 2021-06-19 16:59:07 UTC

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

As of 2021-06-18, IPDH is reporting 149 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-18 |                   93.4 |                             3.0 |                 17.8% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   14.6 |                             3.0 |                 10.1% |
|          Linn |                    8.6 |                             3.8 |                \-8.2% |
|         Scott |                    4.0 |                             2.3 |                 12.9% |
|       Johnson |                    3.0 |                             2.0 |                 55.6% |
|    Black Hawk |                   15.1 |                            11.5 |                 39.5% |
|      Woodbury |                    2.1 |                             2.1 |                  0.0% |
|       Dubuque |                    2.7 |                             2.8 |                  0.0% |
|         Story |                    1.1 |                             1.2 |                  0.0% |
|        Dallas |                    1.4 |                             1.5 |               \-22.7% |
| Pottawattamie |                    2.1 |                             2.3 |                \-4.4% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |                \-7.7% |
|  Black Hawk |                   15.1 |                            11.5 |                 39.5% |
|    Ringgold |                    0.4 |                             8.8 |                 11.1% |
|  Winneshiek |                    1.7 |                             8.6 |                216.7% |
|      Benton |                    2.0 |                             7.8 |                 91.0% |
|       Worth |                    0.6 |                             7.7 |                 57.1% |
| Cerro Gordo |                    3.0 |                             7.1 |                 40.0% |
|       Mills |                    1.0 |                             6.6 |                 55.5% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|      Keokuk |                    0.6 |                             5.6 |                 57.1% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Winneshiek |                    1.7 |                             8.6 |                216.7% |
|      Benton |                    2.0 |                             7.8 |                 91.0% |
|    Crawford |                    0.6 |                             3.4 |                 83.3% |
| Buena Vista |                    1.3 |                             6.6 |                 77.8% |
|       Henry |                    1.0 |                             5.0 |                 75.0% |
|    Marshall |                    0.6 |                             1.4 |                 57.1% |
|      Butler |                    0.6 |                             4.0 |                 57.1% |
|      Keokuk |                    0.6 |                             5.6 |                 57.1% |
|       Worth |                    0.6 |                             7.7 |                 57.1% |
|     Johnson |                    3.0 |                             2.0 |                 55.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    0.0 |                             0.0 |               \-50.0% |
|    Clayton |                    0.0 |                             0.0 |               \-46.1% |
|    Clinton |                    0.3 |                             0.6 |               \-43.7% |
| Washington |                    0.0 |                             0.0 |               \-36.3% |
|     Warren |                    1.1 |                             2.2 |               \-34.8% |
|     Howard |                  \-0.1 |                           \-1.6 |               \-33.4% |
|     Marion |                    0.1 |                             0.4 |               \-33.3% |
|      Union |                    0.1 |                             1.2 |               \-33.3% |
|     Louisa |                    0.1 |                             1.3 |               \-33.3% |
|   Harrison |                    0.0 |                             0.0 |               \-30.0% |
