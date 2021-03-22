Compiled at 2021-03-22 20:23:21 UTC

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

## Tables as of 2021-03-22

As of 2021-03-22, IPDH is reporting 138 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   91.3 |                            18.6 |                \-7.1% |
|          Linn |                   16.0 |                             7.1 |                 20.2% |
|         Scott |                   24.9 |                            14.4 |                  8.4% |
|       Johnson |                   13.6 |                             9.0 |                 39.7% |
|    Black Hawk |                    9.7 |                             7.4 |               \-36.4% |
|      Woodbury |                   27.4 |                            26.6 |                \-7.0% |
|       Dubuque |                    8.0 |                             8.2 |                  0.0% |
|         Story |                   13.3 |                            13.7 |                \-6.5% |
|        Dallas |                   14.0 |                            15.0 |               \-24.5% |
| Pottawattamie |                   16.4 |                            17.6 |                 32.6% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.6 |                            55.5 |                 27.6% |
|      Clay |                    5.6 |                            34.8 |               \-16.4% |
|   O’Brien |                    4.6 |                            33.2 |                 44.4% |
|     Wayne |                    2.0 |                            31.1 |                \-4.5% |
|       Ida |                    2.0 |                            29.2 |               \-40.0% |
|  Woodbury |                   27.4 |                            26.6 |                \-7.0% |
|     Emmet |                    2.4 |                            26.4 |                 26.3% |
|  Plymouth |                    6.6 |                            26.1 |                 10.4% |
|     Mills |                    3.6 |                            23.6 |                 28.0% |
|   Fremont |                    1.6 |                            22.6 |                200.0% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Fremont |                    1.6 |                            22.6 |                200.0% |
|      Humboldt |                    1.9 |                            19.4 |                 53.9% |
|     Appanoose |                    1.1 |                             9.2 |                 50.0% |
|         Sioux |                    7.9 |                            22.5 |                 47.6% |
|      Harrison |                    2.1 |                            15.3 |                 46.7% |
|       O’Brien |                    4.6 |                            33.2 |                 44.4% |
|         Worth |                    0.9 |                            11.6 |                 44.4% |
|       Johnson |                   13.6 |                             9.0 |                 39.7% |
|       Calhoun |                    1.7 |                            17.7 |                 35.7% |
| Pottawattamie |                   16.4 |                            17.6 |                 32.6% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Benton |                    1.0 |                             3.9 |               \-62.2% |
|     Madison |                    1.6 |                             9.6 |               \-60.0% |
|     Carroll |                    1.4 |                             7.1 |               \-59.5% |
|        Page |                    1.7 |                            11.3 |               \-55.8% |
|       Cedar |                    1.1 |                             6.1 |               \-54.5% |
|      Clarke |                    0.3 |                             3.0 |               \-52.6% |
|      Marion |                    2.3 |                             6.9 |               \-51.1% |
|   Allamakee |                    0.9 |                             6.3 |               \-50.0% |
|   Winnebago |                    0.9 |                             8.3 |               \-50.0% |
| Cerro Gordo |                    2.1 |                             5.0 |               \-43.6% |
