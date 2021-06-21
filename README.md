Compiled at 2021-06-21 17:32:57 UTC

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

## Tables as of 2021-06-21

As of 2021-06-21, IPDH is reporting 30 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   10.9 |                             2.2 |               \-13.5% |
|          Linn |                    5.4 |                             2.4 |               \-25.0% |
|         Scott |                    3.0 |                             1.7 |                  3.7% |
|       Johnson |                    2.0 |                             1.3 |               \-12.5% |
|    Black Hawk |                   12.6 |                             9.6 |                \-7.8% |
|      Woodbury |                    1.6 |                             1.5 |               \-21.8% |
|       Dubuque |                    1.9 |                             1.9 |               \-31.0% |
|         Story |                    1.7 |                             1.8 |                 35.7% |
|        Dallas |                    0.9 |                             0.9 |               \-40.9% |
| Pottawattamie |                    1.6 |                             1.7 |               \-28.0% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |               \-14.3% |
|  Black Hawk |                   12.6 |                             9.6 |                \-7.8% |
| Buena Vista |                    1.4 |                             7.3 |                183.4% |
|    Buchanan |                    1.3 |                             6.1 |                 14.3% |
|  Winneshiek |                    1.1 |                             5.7 |                 25.0% |
|      Bremer |                    1.3 |                             5.1 |                 60.0% |
|      Benton |                    1.3 |                             5.0 |                 14.3% |
|   Chickasaw |                    0.6 |                             4.8 |                 37.4% |
|       Mills |                    0.7 |                             4.7 |                  0.0% |
|      Keokuk |                    0.4 |                             4.2 |                 42.9% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                    0.7 |                             3.5 |                299.5% |
| Buena Vista |                    1.4 |                             7.3 |                183.4% |
|       Henry |                    0.7 |                             3.6 |                 71.4% |
|      Bremer |                    1.3 |                             5.1 |                 60.0% |
|       Jones |                    0.4 |                             2.1 |                 42.9% |
|      Keokuk |                    0.4 |                             4.2 |                 42.9% |
|    Marshall |                    0.6 |                             1.4 |                 37.4% |
|   Chickasaw |                    0.6 |                             4.8 |                 37.4% |
|       Story |                    1.7 |                             1.8 |                 35.7% |
|       Sioux |                    1.0 |                             2.9 |                 27.3% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Warren |                    0.3 |                             0.6 |               \-55.0% |
|   Cerro Gordo |                    1.0 |                             2.4 |               \-48.1% |
|          Page |                    0.0 |                             0.0 |               \-46.1% |
|        Dallas |                    0.9 |                             0.9 |               \-40.9% |
|         Cedar |                    0.3 |                             1.5 |               \-40.0% |
|           Lee |                    0.7 |                             2.1 |               \-36.8% |
|       Dubuque |                    1.9 |                             1.9 |               \-31.0% |
|      Hamilton |                    0.3 |                             1.9 |               \-30.7% |
| Pottawattamie |                    1.6 |                             1.7 |               \-28.0% |
|        Marion |                    0.1 |                             0.4 |               \-27.2% |
