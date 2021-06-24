Compiled at 2021-06-24 20:09:33 UTC

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

## Tables as of 2021-06-24

As of 2021-06-24, IPDH is reporting 62 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    8.6 |                             1.7 |               \-23.0% |
|          Linn |                    6.7 |                             3.0 |               \-11.5% |
|         Scott |                    1.6 |                             0.9 |               \-47.1% |
|       Johnson |                    1.3 |                             0.9 |               \-40.7% |
|    Black Hawk |                   14.1 |                            10.8 |                  4.9% |
|      Woodbury |                    0.7 |                             0.7 |               \-53.9% |
|       Dubuque |                    2.1 |                             2.2 |               \-26.7% |
|         Story |                    0.7 |                             0.7 |               \-20.0% |
|        Dallas |                    1.1 |                             1.2 |               \-25.0% |
| Pottawattamie |                    1.7 |                             1.8 |               \-17.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Monona |                    1.1 |                            13.3 |                114.3% |
| Black Hawk |                   14.1 |                            10.8 |                  4.9% |
|       Lyon |                    0.7 |                             6.1 |                 71.4% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
|    Webster |                    2.1 |                             6.0 |                 29.4% |
|      Worth |                    0.4 |                             5.8 |                 11.1% |
|   Marshall |                    2.1 |                             5.4 |                119.9% |
|     Benton |                    1.3 |                             5.0 |                  0.0% |
|      Henry |                    1.0 |                             5.0 |                 16.7% |
| Winneshiek |                    1.0 |                             5.0 |               \-12.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Marshall |                    2.1 |                             5.4 |                119.9% |
|     Monona |                    1.1 |                            13.3 |                114.3% |
|       Lyon |                    0.7 |                             6.1 |                 71.4% |
|      Sioux |                    1.1 |                             3.3 |                 66.6% |
|     Howard |                    0.3 |                             3.1 |                 50.1% |
|     Wright |                    0.4 |                             3.4 |                 42.9% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
| Des Moines |                    1.4 |                             3.7 |                 41.7% |
|     Bremer |                    1.1 |                             4.6 |                 36.4% |
|    Webster |                    2.1 |                             6.0 |                 29.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                  \-0.3 |                           \-5.2 |               \-68.8% |
|    Woodbury |                    0.7 |                             0.7 |               \-53.9% |
| Cerro Gordo |                    0.9 |                             2.0 |               \-48.0% |
|       Scott |                    1.6 |                             0.9 |               \-47.1% |
| Buena Vista |                    0.1 |                             0.7 |               \-46.7% |
|       Mills |                    0.1 |                             0.9 |               \-46.7% |
|    Crawford |                    0.0 |                             0.0 |               \-41.7% |
|     Johnson |                    1.3 |                             0.9 |               \-40.7% |
|         Lee |                    0.6 |                             1.7 |               \-38.9% |
|       Cedar |                    0.1 |                             0.8 |               \-33.3% |
