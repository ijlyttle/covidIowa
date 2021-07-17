Compiled at 2021-07-17 20:14:42 UTC

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

## Tables as of 2021-07-17

As of 2021-07-17, IPDH is reporting 179 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   18.7 |                             3.8 |               \-50.7% |
|          Linn |                    5.3 |                             2.3 |               \-51.1% |
|         Scott |                    7.4 |                             4.3 |                391.8% |
|       Johnson |                    4.1 |                             2.7 |                  0.0% |
|    Black Hawk |                   18.3 |                            13.9 |                \-8.8% |
|      Woodbury |                    6.4 |                             6.2 |            \-1 401.1% |
|       Dubuque |                    1.7 |                             1.8 |               \-47.2% |
|         Story |                    3.4 |                             3.5 |               \-41.5% |
|        Dallas |                    3.7 |                             4.0 |               \-60.2% |
| Pottawattamie |                    4.3 |                             4.6 |                117.6% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Calhoun |                    3.1 |                            32.5 |                 52.7% |
|  Webster |                   10.6 |                            29.4 |                 58.8% |
|   Monroe |                    1.9 |                            24.1 |               \-13.1% |
| Franklin |                    2.3 |                            22.7 |                \-8.0% |
|  Decatur |                    1.6 |                            20.0 |               \-37.9% |
|   Wright |                    2.4 |                            19.3 |                242.9% |
| Humboldt |                    1.7 |                            17.9 |               \-17.4% |
|  Hancock |                    1.9 |                            17.5 |                 17.6% |
|    Adair |                    1.1 |                            16.0 |                  0.0% |
|    Adams |                    0.6 |                            15.9 |                998.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Mills |                    0.0 |                             0.0 |                   Inf |
|      Union |                    0.1 |                             1.2 |                   Inf |
|    Audubon |                    0.0 |                             0.0 |                   Inf |
|      Adams |                    0.6 |                            15.9 |                998.6% |
|     Marion |                    2.3 |                             6.9 |                475.5% |
|      Scott |                    7.4 |                             4.3 |                391.8% |
|       Cass |                    1.9 |                            14.5 |                300.1% |
| Winneshiek |                    0.7 |                             3.6 |                299.5% |
|     Wright |                    2.4 |                            19.3 |                242.9% |
|      Jones |                    0.3 |                             1.4 |                199.8% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Woodbury |                    6.4 |                             6.2 |            \-1 401.1% |
|     Worth |                    0.1 |                             1.9 |              \-899.3% |
|     Lucas |                    0.3 |                             3.3 |              \-549.7% |
|    Shelby |                    1.3 |                            11.2 |              \-366.7% |
|   Carroll |                    0.6 |                             2.8 |              \-209.9% |
|   Mahaska |                    1.1 |                             5.2 |              \-207.1% |
| Appanoose |                    0.3 |                             2.3 |              \-200.0% |
|      Iowa |                    0.1 |                             0.9 |              \-157.1% |
|    Jasper |                    1.4 |                             3.8 |               \-94.2% |
|     Henry |                    0.4 |                             2.1 |               \-82.1% |
