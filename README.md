Compiled at 2021-07-19 20:15:07 UTC

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

## Tables as of 2021-07-19

As of 2021-07-19, IPDH is reporting 141 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   21.0 |                             4.3 |               \-46.0% |
|          Linn |                    5.4 |                             2.4 |               \-54.1% |
|         Scott |                    8.4 |                             4.9 |                340.0% |
|       Johnson |                    6.4 |                             4.3 |                 36.8% |
|    Black Hawk |                   18.9 |                            14.4 |                \-9.2% |
|      Woodbury |                    7.0 |                             6.8 |            \-1 501.1% |
|       Dubuque |                    2.1 |                             2.2 |               \-40.5% |
|         Story |                    4.4 |                             4.6 |               \-28.3% |
|        Dallas |                    4.7 |                             5.0 |               \-53.5% |
| Pottawattamie |                    4.9 |                             5.2 |                105.0% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Webster |                   11.4 |                            31.8 |                 55.4% |
|   Monroe |                    2.3 |                            29.7 |                \-8.0% |
|  Calhoun |                    2.6 |                            26.6 |                  8.7% |
| Hamilton |                    3.0 |                            20.3 |                 21.7% |
|    Adair |                    1.4 |                            20.0 |                 13.3% |
| Franklin |                    2.0 |                            19.9 |               \-19.2% |
| Humboldt |                    1.9 |                            19.4 |               \-13.1% |
|   Wright |                    2.3 |                            18.2 |                130.0% |
|  Decatur |                    1.3 |                            16.3 |               \-48.4% |
|  Hancock |                    1.7 |                            16.1 |                  5.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Mills |                    0.1 |                             0.9 |                   Inf |
|      Union |                    0.0 |                             0.0 |                   Inf |
|      Worth |                    0.0 |                             0.0 |                   Inf |
|    Audubon |                    0.0 |                             0.0 |                   Inf |
|      Adams |                    0.4 |                            11.9 |                899.3% |
|     Marion |                    3.0 |                             9.0 |                366.7% |
|      Scott |                    8.4 |                             4.9 |                340.0% |
| Winneshiek |                    0.7 |                             3.6 |                299.5% |
|       Cass |                    1.9 |                            14.5 |                233.4% |
|     Butler |                    0.7 |                             4.9 |                140.1% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Woodbury |                    7.0 |                             6.8 |            \-1 501.1% |
|     Lucas |                    0.4 |                             5.0 |              \-599.7% |
|    Shelby |                    1.1 |                            10.0 |              \-475.3% |
|   Mahaska |                    1.6 |                             7.1 |              \-220.0% |
|   Carroll |                    0.7 |                             3.5 |              \-219.9% |
| Appanoose |                    0.3 |                             2.3 |              \-200.0% |
|      Iowa |                    0.1 |                             0.9 |              \-150.0% |
|    Jasper |                    1.9 |                             5.0 |               \-93.1% |
|     Henry |                    0.7 |                             3.6 |               \-77.8% |
|   Fremont |                    0.1 |                             2.1 |               \-69.2% |
