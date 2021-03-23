Compiled at 2021-03-23 17:16:41 UTC

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

## Tables as of 2021-03-23

As of 2021-03-23, IPDH is reporting 489 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   92.0 |                            18.8 |                \-4.0% |
|          Linn |                   16.4 |                             7.2 |                 20.8% |
|         Scott |                   28.9 |                            16.7 |                 30.6% |
|       Johnson |                   13.9 |                             9.2 |                 40.5% |
|    Black Hawk |                   10.4 |                             7.9 |               \-29.2% |
|      Woodbury |                   28.0 |                            27.2 |                \-6.9% |
|       Dubuque |                    9.1 |                             9.4 |                  9.2% |
|         Story |                   13.3 |                            13.7 |                \-3.8% |
|        Dallas |                   15.6 |                            16.7 |               \-14.7% |
| Pottawattamie |                   16.1 |                            17.3 |                 20.0% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    8.4 |                            48.8 |                \-7.0% |
|      Clay |                    7.1 |                            44.6 |                 18.8% |
|     Wayne |                    2.3 |                            35.5 |                  4.5% |
|   O’Brien |                    4.1 |                            30.1 |                 20.0% |
|  Woodbury |                   28.0 |                            27.2 |                \-6.9% |
|       Ida |                    1.9 |                            27.1 |               \-31.0% |
|     Emmet |                    2.4 |                            26.4 |                  9.1% |
|  Plymouth |                    6.3 |                            25.0 |                 10.9% |
|  Cherokee |                    2.7 |                            24.2 |               \-39.5% |
|   Guthrie |                    2.4 |                            22.7 |                100.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Fremont |                    1.6 |                            22.6 |                200.0% |
|   Guthrie |                    2.4 |                            22.7 |                100.1% |
|   Osceola |                    1.3 |                            21.6 |                 77.8% |
|     Worth |                    1.0 |                            13.5 |                 75.0% |
|  Humboldt |                    1.9 |                            19.4 |                 53.9% |
| Van Buren |                    0.3 |                             4.1 |                 50.1% |
|  Buchanan |                    3.3 |                            15.5 |                 50.0% |
|   Johnson |                   13.9 |                             9.2 |                 40.5% |
| Appanoose |                    1.1 |                             9.2 |                 36.4% |
|    Butler |                    1.3 |                             8.9 |                 33.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Shelby |                    0.7 |                             6.2 |               \-62.5% |
|     Benton |                    1.0 |                             3.9 |               \-57.6% |
|       Lyon |                    1.0 |                             8.5 |               \-50.0% |
|      Cedar |                    1.0 |                             5.4 |               \-48.1% |
|  Winnebago |                    0.9 |                             8.3 |               \-48.0% |
|     Clarke |                    0.3 |                             3.0 |               \-47.1% |
| Washington |                    1.3 |                             5.9 |               \-46.7% |
|    Carroll |                    2.0 |                             9.9 |               \-46.1% |
|       Page |                    2.0 |                            13.2 |               \-44.7% |
|     Bremer |                    1.3 |                             5.1 |               \-42.8% |
