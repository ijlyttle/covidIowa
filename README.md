Compiled at 2021-03-17 03:37:40 UTC

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

## Tables as of 2021-03-16

As of 2021-03-16, IPDH is reporting 414 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   95.9 |                            19.6 |                \-8.4% |
|          Linn |                   13.4 |                             5.9 |               \-20.5% |
|         Scott |                   21.9 |                            12.6 |                \-6.4% |
|       Johnson |                    9.6 |                             6.3 |               \-38.3% |
|    Black Hawk |                   15.1 |                            11.5 |                  1.8% |
|      Woodbury |                   30.1 |                            29.2 |                 29.8% |
|       Dubuque |                    8.3 |                             8.5 |               \-21.7% |
|         Story |                   13.9 |                            14.3 |               \-31.1% |
|        Dallas |                   18.4 |                            19.7 |                \-6.8% |
| Pottawattamie |                   13.3 |                            14.3 |               \-14.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.1 |                            53.0 |                 82.1% |
|       Ida |                    3.1 |                            45.8 |                  3.6% |
|  Cherokee |                    5.1 |                            45.8 |                 38.7% |
|      Clay |                    5.9 |                            36.6 |                 37.1% |
|     Wayne |                    2.1 |                            33.3 |               \-33.3% |
|    Shelby |                    3.6 |                            31.2 |                \-3.0% |
|      Page |                    4.4 |                            29.3 |                 40.8% |
|  Woodbury |                   30.1 |                            29.2 |                 29.8% |
|   Kossuth |                    3.9 |                            26.0 |                 70.0% |
|      Lyon |                    3.0 |                            25.5 |                133.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Lyon |                    3.0 |                            25.5 |                133.4% |
|    Carroll |                    4.6 |                            22.7 |                 95.0% |
|  Dickinson |                    9.1 |                            53.0 |                 82.1% |
| Pocahontas |                    1.3 |                            19.4 |                 77.8% |
| Washington |                    3.3 |                            15.0 |                 76.5% |
|    Kossuth |                    3.9 |                            26.0 |                 70.0% |
|     Monona |                    1.6 |                            18.2 |                 63.7% |
|      Mills |                    2.6 |                            17.0 |                 47.0% |
|       Page |                    4.4 |                            29.3 |                 40.8% |
|   Cherokee |                    5.1 |                            45.8 |                 38.7% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Fayette |                    0.7 |                             3.6 |               \-65.7% |
|   Madison |                    2.0 |                            12.2 |               \-61.1% |
|   Fremont |                  \-0.1 |                           \-2.1 |               \-57.2% |
| Allamakee |                    2.1 |                            15.7 |               \-56.9% |
| Chickasaw |                    0.4 |                             3.6 |               \-50.0% |
|   Guthrie |                    0.7 |                             6.7 |               \-50.0% |
|   Decatur |                    0.4 |                             5.5 |               \-50.0% |
|      Cass |                    2.0 |                            15.6 |               \-47.5% |
|     Worth |                    0.1 |                             1.9 |               \-46.7% |
|  Buchanan |                    1.9 |                             8.8 |               \-46.0% |
