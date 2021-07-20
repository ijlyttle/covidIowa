Compiled at 2021-07-20 20:16:48 UTC

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

## Tables as of 2021-07-20

As of 2021-07-20, IPDH is reporting 249 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   24.4 |                             5.0 |               \-40.5% |
|          Linn |                    6.6 |                             2.9 |               \-44.2% |
|         Scott |                    7.4 |                             4.3 |                103.5% |
|       Johnson |                    6.6 |                             4.3 |                 29.3% |
|    Black Hawk |                   20.4 |                            15.6 |                \-8.0% |
|      Woodbury |                    6.4 |                             6.2 |                940.5% |
|       Dubuque |                    2.1 |                             2.2 |               \-43.6% |
|         Story |                    6.3 |                             6.5 |                  0.0% |
|        Dallas |                    6.0 |                             6.4 |               \-45.6% |
| Pottawattamie |                    5.0 |                             5.4 |                 68.0% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Webster |                   12.7 |                            35.4 |                 65.5% |
|   Monroe |                    2.3 |                            29.7 |               \-11.5% |
|  Calhoun |                    2.4 |                            25.1 |                  4.4% |
| Humboldt |                    2.1 |                            22.4 |                \-8.3% |
| Hamilton |                    3.3 |                            22.2 |                 20.0% |
|   Wright |                    2.6 |                            20.5 |                127.3% |
|    Adair |                    1.4 |                            20.0 |                 13.3% |
|    Adams |                    0.7 |                            19.8 |              1 098.6% |
| Franklin |                    1.7 |                            17.0 |               \-26.9% |
|  Decatur |                    1.3 |                            16.3 |               \-51.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Mills |                    0.1 |                             0.9 |                   Inf |
|      Union |                    0.0 |                             0.0 |                   Inf |
|      Adams |                    0.7 |                            19.8 |              1 098.6% |
|   Woodbury |                    6.4 |                             6.2 |                940.5% |
| Winneshiek |                    0.7 |                             3.6 |                299.5% |
|     Marion |                    3.0 |                             9.0 |                211.0% |
|     Wright |                    2.6 |                            20.5 |                127.3% |
|   Ringgold |                    0.3 |                             5.8 |                125.2% |
|     Butler |                    0.9 |                             5.9 |                116.7% |
|      Scott |                    7.4 |                             4.3 |                103.5% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Worth |                    0.0 |                             0.0 |              \-799.3% |
|   Audubon |                    0.0 |                             0.0 |              \-799.3% |
|     Lucas |                    0.4 |                             5.0 |              \-599.7% |
|    Shelby |                    0.9 |                             7.5 |              \-532.9% |
|   Mahaska |                    1.9 |                             8.4 |              \-242.9% |
|   Carroll |                    0.9 |                             4.2 |              \-230.0% |
| Appanoose |                    0.4 |                             3.5 |              \-211.1% |
|      Iowa |                    0.1 |                             0.9 |              \-150.0% |
|    Jasper |                    2.1 |                             5.8 |               \-92.4% |
|     Henry |                    0.6 |                             2.9 |               \-80.0% |
