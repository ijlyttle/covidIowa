Compiled at 2021-06-25 23:53:49 UTC

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

## Tables as of 2021-06-25

As of 2021-06-25, IPDH is reporting 69 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    8.0 |                             1.6 |               \-29.2% |
|          Linn |                    6.6 |                             2.9 |                \-8.6% |
|         Scott |                    1.4 |                             0.8 |               \-46.9% |
|       Johnson |                    1.3 |                             0.9 |               \-38.4% |
|    Black Hawk |                   14.6 |                            11.1 |                  9.0% |
|      Woodbury |                    0.6 |                             0.6 |               \-47.6% |
|       Dubuque |                    1.7 |                             1.8 |               \-24.0% |
|         Story |                    1.0 |                             1.0 |                  0.0% |
|        Dallas |                    1.3 |                             1.4 |               \-11.1% |
| Pottawattamie |                    1.6 |                             1.7 |               \-14.3% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Monona |                    1.1 |                            13.3 |                114.3% |
| Black Hawk |                   14.6 |                            11.1 |                  9.0% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|    Webster |                    2.9 |                             8.0 |                 68.7% |
|      Adams |                    0.3 |                             7.9 |                 28.6% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
|     Keokuk |                    0.6 |                             5.6 |                 37.4% |
|     Benton |                    1.3 |                             5.0 |               \-20.0% |
|      Henry |                    1.0 |                             5.0 |                 27.3% |
| Des Moines |                    1.9 |                             4.8 |                 66.7% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Monona |                    1.1 |                            13.3 |                114.3% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|   Marshall |                    1.9 |                             4.7 |                 81.9% |
|    Webster |                    2.9 |                             8.0 |                 68.7% |
| Des Moines |                    1.9 |                             4.8 |                 66.7% |
|     Howard |                    0.3 |                             3.1 |                 50.1% |
|     Wright |                    0.4 |                             3.4 |                 42.9% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
|     Keokuk |                    0.6 |                             5.6 |                 37.4% |
|     Clarke |                    0.3 |                             3.0 |                 28.6% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                  \-0.1 |                           \-0.7 |               \-62.5% |
|    Crawford |                  \-0.1 |                           \-0.8 |               \-60.0% |
| Cerro Gordo |                    0.6 |                             1.3 |               \-59.3% |
|     Audubon |                  \-0.1 |                           \-2.6 |               \-53.9% |
|    Woodbury |                    0.6 |                             0.6 |               \-47.6% |
|       Scott |                    1.4 |                             0.8 |               \-46.9% |
|       Mills |                    0.3 |                             1.9 |               \-40.0% |
|     Johnson |                    1.3 |                             0.9 |               \-38.4% |
|  Winneshiek |                    0.9 |                             4.3 |               \-35.0% |
|      Jasper |                    0.3 |                             0.8 |               \-30.7% |
