Compiled at 2021-07-16 17:26:04 UTC

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

## Tables as of 2021-07-16

As of 2021-07-16, IPDH is reporting 206 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   19.1 |                             3.9 |               \-47.8% |
|          Linn |                    5.3 |                             2.3 |               \-48.8% |
|         Scott |                    6.7 |                             3.9 |                285.7% |
|       Johnson |                    3.4 |                             2.3 |                \-6.0% |
|    Black Hawk |                   17.4 |                            13.3 |                \-7.9% |
|      Woodbury |                    5.4 |                             5.3 |            \-1 225.9% |
|       Dubuque |                    2.1 |                             2.2 |               \-33.3% |
|         Story |                    2.7 |                             2.8 |               \-50.0% |
|        Dallas |                    3.6 |                             3.8 |               \-60.5% |
| Pottawattamie |                    3.3 |                             3.5 |                114.3% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Webster |                   10.9 |                            30.2 |                 84.4% |
|  Calhoun |                    2.7 |                            28.1 |                 44.5% |
|  Hancock |                    2.1 |                            20.2 |                 57.1% |
|   Wright |                    2.4 |                            19.3 |                300.1% |
|   Monroe |                    1.4 |                            18.5 |               \-19.0% |
| Franklin |                    1.9 |                            18.4 |               \-23.1% |
|  Decatur |                    1.4 |                            18.2 |               \-45.2% |
| Hamilton |                    2.6 |                            17.4 |                 38.9% |
|   Monona |                    1.4 |                            16.6 |                \-5.5% |
|    Adams |                    0.6 |                            15.9 |                998.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.0 |                             0.0 |                   Inf |
|     Marion |                    2.6 |                             7.7 |              2 397.2% |
|      Adams |                    0.6 |                            15.9 |                998.6% |
|      Mills |                    0.0 |                             0.0 |                599.3% |
|     Wright |                    2.4 |                            19.3 |                300.1% |
|      Scott |                    6.7 |                             3.9 |                285.7% |
|       Cass |                    1.6 |                            12.2 |                260.1% |
| Winneshiek |                    0.6 |                             2.9 |                175.1% |
|      Jones |                    0.1 |                             0.7 |                166.4% |
|   Mitchell |                    0.9 |                             8.1 |                116.7% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Woodbury |                    5.4 |                             5.3 |            \-1 225.9% |
|     Union |                    0.3 |                             2.3 |              \-999.3% |
|     Worth |                    0.1 |                             1.9 |              \-899.3% |
|     Lucas |                    0.3 |                             3.3 |              \-549.7% |
|    Shelby |                    1.3 |                            11.2 |              \-500.4% |
|   Mahaska |                    1.0 |                             4.5 |              \-216.7% |
|   Carroll |                    0.4 |                             2.1 |              \-200.0% |
| Appanoose |                    0.1 |                             1.2 |              \-188.9% |
|      Iowa |                    0.0 |                             0.0 |              \-150.0% |
|    Jasper |                    1.1 |                             3.1 |               \-94.9% |
