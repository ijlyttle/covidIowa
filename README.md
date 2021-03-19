Compiled at 2021-03-19 00:00:14 UTC

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

## Tables as of 2021-03-18

As of 2021-03-18, IPDH is reporting 969 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   92.3 |                            18.8 |               \-18.5% |
|          Linn |                   14.6 |                             6.4 |                \-6.0% |
|         Scott |                   19.3 |                            11.2 |               \-33.6% |
|       Johnson |                   10.6 |                             7.0 |               \-23.6% |
|    Black Hawk |                   11.4 |                             8.7 |               \-33.1% |
|      Woodbury |                   28.4 |                            27.6 |                  4.6% |
|       Dubuque |                    7.0 |                             7.2 |               \-32.5% |
|         Story |                   12.0 |                            12.4 |               \-37.2% |
|        Dallas |                   15.6 |                            16.7 |               \-20.0% |
| Pottawattamie |                   14.1 |                            15.2 |               \-13.8% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.0 |                            52.1 |                 32.1% |
|  Cherokee |                    4.0 |                            35.6 |                  2.9% |
|       Ida |                    2.3 |                            33.3 |               \-37.8% |
|     Wayne |                    2.1 |                            33.3 |               \-37.1% |
|     Emmet |                    3.0 |                            32.6 |                 55.6% |
|      Clay |                    4.7 |                            29.4 |               \-24.5% |
|   O’Brien |                    4.0 |                            29.1 |                  0.0% |
|   Kossuth |                    4.1 |                            28.0 |                 63.6% |
|  Woodbury |                   28.4 |                            27.6 |                  4.6% |
|  Plymouth |                    6.3 |                            25.0 |                  8.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Fremont |                    1.1 |                            16.4 |                150.1% |
|     Taylor |                    0.3 |                             4.7 |                 80.1% |
| Pocahontas |                    1.3 |                            19.4 |                 77.8% |
|    Kossuth |                    4.1 |                            28.0 |                 63.6% |
| Washington |                    2.7 |                            12.4 |                 62.5% |
|      Emmet |                    3.0 |                            32.6 |                 55.6% |
|   Hamilton |                    1.1 |                             7.7 |                 50.0% |
|    Clayton |                    1.7 |                             9.8 |                 46.1% |
|    Carroll |                    4.1 |                            20.5 |                 38.5% |
|  Dickinson |                    9.0 |                            52.1 |                 32.1% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|        Page |                    1.1 |                             7.6 |               \-67.4% |
|     Madison |                    1.9 |                            11.4 |               \-63.6% |
|     Fayette |                    0.6 |                             2.9 |               \-60.7% |
|      Jasper |                    2.3 |                             6.1 |               \-58.2% |
|      Benton |                    2.1 |                             8.4 |               \-54.2% |
|      Louisa |                    0.1 |                             1.3 |               \-52.9% |
|      Marion |                    3.0 |                             9.0 |               \-50.0% |
|   Allamakee |                    2.0 |                            14.6 |               \-50.0% |
|    Marshall |                    3.3 |                             8.3 |               \-45.4% |
| Cerro Gordo |                    3.1 |                             7.4 |               \-45.3% |
