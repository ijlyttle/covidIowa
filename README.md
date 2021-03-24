Compiled at 2021-03-24 17:38:28 UTC

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

## Tables as of 2021-03-24

As of 2021-03-24, IPDH is reporting 766 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  114.7 |                            23.4 |                 62.6% |
|          Linn |                   19.7 |                             8.7 |                 79.0% |
|         Scott |                   37.4 |                            21.6 |                144.6% |
|       Johnson |                   18.0 |                            11.9 |                118.0% |
|    Black Hawk |                   13.6 |                            10.3 |                 25.9% |
|      Woodbury |                   34.0 |                            33.0 |                 41.6% |
|       Dubuque |                   12.3 |                            12.6 |                 97.9% |
|         Story |                   16.6 |                            17.1 |                 66.2% |
|        Dallas |                   19.0 |                            20.3 |                 37.3% |
| Pottawattamie |                   21.7 |                            23.3 |                 93.9% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.1 |                            64.6 |                 39.4% |
|      Clay |                    8.4 |                            52.6 |                 94.1% |
|     Wayne |                    2.7 |                            42.1 |                 30.0% |
|     Emmet |                    3.9 |                            41.9 |                 88.9% |
|   O’Brien |                    5.4 |                            39.5 |                 60.7% |
|       Ida |                    2.4 |                            35.4 |                 26.3% |
|  Woodbury |                   34.0 |                            33.0 |                 41.6% |
|   Fremont |                    2.3 |                            32.8 |              1 049.0% |
|  Cherokee |                    3.6 |                            31.8 |                \-3.0% |
|  Plymouth |                    7.4 |                            29.5 |                 43.9% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Fremont |                    2.3 |                            32.8 |              1 049.0% |
|         Scott |                   37.4 |                            21.6 |                144.6% |
|       Guthrie |                    2.6 |                            24.1 |                127.3% |
|       Johnson |                   18.0 |                            11.9 |                118.0% |
|       Osceola |                    1.7 |                            28.8 |                111.0% |
|        Jasper |                    5.6 |                            15.0 |                100.0% |
|       Dubuque |                   12.3 |                            12.6 |                 97.9% |
|          Clay |                    8.4 |                            52.6 |                 94.1% |
| Pottawattamie |                   21.7 |                            23.3 |                 93.9% |
|      Humboldt |                    2.6 |                            26.9 |                 92.3% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Clarke |                    0.3 |                             3.0 |               \-40.0% |
|     Benton |                    1.6 |                             6.1 |               \-35.7% |
|      Cedar |                    1.3 |                             6.9 |               \-33.3% |
|    Carroll |                    2.4 |                            12.0 |               \-29.4% |
|  Winnebago |                    1.3 |                            12.4 |               \-27.3% |
|       Lyon |                    1.7 |                            14.6 |               \-24.0% |
| Washington |                    1.9 |                             8.5 |               \-23.1% |
|     Shelby |                    1.6 |                            13.7 |               \-21.8% |
|     Bremer |                    1.9 |                             7.4 |               \-20.0% |
| Pocahontas |                    0.7 |                            10.8 |               \-14.3% |
