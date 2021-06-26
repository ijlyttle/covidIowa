Compiled at 2021-06-26 23:53:07 UTC

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

## Tables as of 2021-06-26

As of 2021-06-26, IPDH is reporting 78 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    5.4 |                             1.1 |               \-45.8% |
|          Linn |                    5.6 |                             2.5 |               \-19.3% |
|         Scott |                    1.6 |                             0.9 |               \-37.9% |
|       Johnson |                    2.1 |                             1.4 |                 15.8% |
|    Black Hawk |                   15.7 |                            12.0 |                 25.8% |
|      Woodbury |                    0.6 |                             0.6 |               \-42.1% |
|       Dubuque |                    1.9 |                             1.9 |               \-13.1% |
|         Story |                    1.3 |                             1.3 |                  6.7% |
|        Dallas |                    1.4 |                             1.5 |                 54.6% |
| Pottawattamie |                    1.4 |                             1.5 |               \-15.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Black Hawk |                   15.7 |                            12.0 |                 25.8% |
|     Monona |                    1.0 |                            11.6 |                100.0% |
|    Webster |                    3.3 |                             9.2 |                 76.5% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|      Adams |                    0.3 |                             7.9 |                 28.6% |
|     Benton |                    1.6 |                             6.1 |               \-14.3% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
|        Lee |                    1.9 |                             5.5 |                 17.6% |
|   Marshall |                    2.1 |                             5.4 |                100.1% |
|    Audubon |                    0.3 |                             5.2 |               \-25.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Marshall |                    2.1 |                             5.4 |                100.1% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|     Monona |                    1.0 |                            11.6 |                100.0% |
|    Webster |                    3.3 |                             9.2 |                 76.5% |
|     Dallas |                    1.4 |                             1.5 |                 54.6% |
|     Howard |                    0.3 |                             3.1 |                 50.1% |
|     Clarke |                    0.4 |                             4.6 |                 42.9% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
| Des Moines |                    1.9 |                             4.8 |                 42.8% |
|    Kossuth |                    0.1 |                             1.0 |                 33.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    0.0 |                             0.0 |               \-56.3% |
| Cerro Gordo |                    0.7 |                             1.7 |               \-55.6% |
|     Carroll |                  \-0.3 |                           \-1.4 |               \-54.6% |
|        Polk |                    5.4 |                             1.1 |               \-45.8% |
|    Woodbury |                    0.6 |                             0.6 |               \-42.1% |
|       Scott |                    1.6 |                             0.9 |               \-37.9% |
|   Allamakee |                    0.0 |                             0.0 |               \-36.3% |
|     Guthrie |                    0.0 |                             0.0 |               \-36.3% |
|      Warren |                    0.3 |                             0.6 |               \-35.7% |
|   Muscatine |                    0.4 |                             1.0 |               \-33.3% |
