Compiled at 2021-03-17 17:19:38 UTC

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

## Tables as of 2021-03-17

As of 2021-03-17, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   70.1 |                            14.3 |               \-40.4% |
|          Linn |                   10.6 |                             4.7 |               \-36.2% |
|         Scott |                   14.7 |                             8.5 |               \-47.9% |
|       Johnson |                    7.7 |                             5.1 |               \-50.0% |
|    Black Hawk |                   10.6 |                             8.1 |               \-37.2% |
|      Woodbury |                   23.7 |                            23.0 |               \-10.8% |
|       Dubuque |                    5.7 |                             5.9 |               \-50.0% |
|         Story |                    9.6 |                             9.9 |               \-55.2% |
|        Dallas |                   13.6 |                            14.5 |               \-32.9% |
| Pottawattamie |                   10.7 |                            11.5 |               \-37.4% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    7.7 |                            44.7 |                 32.6% |
|  Cherokee |                    3.7 |                            33.1 |                \-5.7% |
|     Wayne |                    1.9 |                            28.8 |               \-41.2% |
|      Page |                    3.9 |                            25.5 |                 30.8% |
|       Ida |                    1.7 |                            25.0 |               \-50.0% |
|   Kossuth |                    3.6 |                            24.1 |                 45.4% |
|      Clay |                    3.9 |                            24.1 |               \-26.1% |
|  Woodbury |                   23.7 |                            23.0 |               \-10.8% |
|      Lyon |                    2.6 |                            21.9 |                 78.6% |
|   O’Brien |                    3.0 |                            21.8 |               \-34.9% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Lyon |                    2.6 |                            21.9 |                 78.6% |
| Washington |                    2.7 |                            12.4 |                 62.5% |
| Pocahontas |                    1.0 |                            15.1 |                 55.5% |
|    Kossuth |                    3.6 |                            24.1 |                 45.4% |
|    Carroll |                    3.9 |                            19.1 |                 41.6% |
|   Delaware |                    2.9 |                            16.8 |                 35.0% |
|  Dickinson |                    7.7 |                            44.7 |                 32.6% |
|       Page |                    3.9 |                            25.5 |                 30.8% |
|    Clayton |                    1.1 |                             6.5 |                 25.0% |
|  Winnebago |                    2.1 |                            20.7 |                 15.8% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Fremont |                  \-0.7 |                          \-10.3 |               \-86.7% |
|   Madison |                    1.4 |                             8.7 |               \-69.6% |
|   Fayette |                    0.6 |                             2.9 |               \-64.5% |
| Allamakee |                    1.7 |                            12.5 |               \-62.8% |
|    Jasper |                    2.3 |                             6.1 |               \-61.0% |
| Palo Alto |                    0.6 |                             6.4 |               \-60.7% |
|  Marshall |                    2.6 |                             6.5 |               \-59.7% |
|    Keokuk |                    0.0 |                             0.0 |               \-58.8% |
|    Marion |                    2.3 |                             6.9 |               \-57.4% |
|     Story |                    9.6 |                             9.9 |               \-55.2% |
