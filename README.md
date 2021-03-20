Compiled at 2021-03-20 23:57:19 UTC

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

## Tables as of 2021-03-20

As of 2021-03-20, IPDH is reporting 448 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |
| 2021-03-18 |                  413.6 |                            13.1 |               \-24.3% |
| 2021-03-17 |                  334.0 |                            10.6 |               \-42.1% |
| 2021-03-16 |                  448.3 |                            14.2 |               \-15.1% |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   94.7 |                            19.3 |                \-2.6% |
|          Linn |                   15.1 |                             6.7 |                 15.3% |
|         Scott |                   23.1 |                            13.4 |                  3.7% |
|       Johnson |                   10.6 |                             7.0 |                \-6.9% |
|    Black Hawk |                   10.1 |                             7.7 |               \-29.1% |
|      Woodbury |                   29.4 |                            28.5 |                  2.9% |
|       Dubuque |                    7.4 |                             7.6 |                \-6.3% |
|         Story |                   12.9 |                            13.2 |               \-14.9% |
|        Dallas |                   14.4 |                            15.4 |               \-21.2% |
| Pottawattamie |                   16.4 |                            17.6 |                 24.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                    9.0 |                            52.1 |                 18.6% |
|   O’Brien |                    4.4 |                            32.2 |                 40.8% |
|   Kossuth |                    4.6 |                            30.9 |                105.3% |
|     Emmet |                    2.7 |                            29.5 |                 52.9% |
|       Ida |                    2.0 |                            29.2 |               \-48.8% |
|  Woodbury |                   29.4 |                            28.5 |                  2.9% |
|      Clay |                    4.6 |                            28.5 |               \-30.4% |
|     Wayne |                    1.6 |                            24.4 |               \-25.0% |
|   Wapello |                    8.3 |                            23.7 |               \-14.5% |
|  Plymouth |                    5.9 |                            23.3 |                \-5.9% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Fremont |                    1.1 |                            16.4 |                150.1% |
|    Kossuth |                    4.6 |                            30.9 |                105.3% |
|  Appanoose |                    1.4 |                            11.5 |                 88.9% |
|      Sioux |                    7.9 |                            22.5 |                 63.1% |
| Montgomery |                    0.6 |                             5.8 |                 57.1% |
|      Emmet |                    2.7 |                            29.5 |                 52.9% |
|    Clayton |                    1.6 |                             9.0 |                 50.0% |
|    O’Brien |                    4.4 |                            32.2 |                 40.8% |
|     Keokuk |                    0.6 |                             5.6 |                 37.4% |
|    Calhoun |                    1.7 |                            17.7 |                 35.7% |

Biggest decline in positive cases, week-over-week:

|  county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------: | ---------------------: | ------------------------------: | --------------------: |
| Madison |                    1.9 |                            11.4 |               \-56.5% |
|  Benton |                    1.4 |                             5.6 |               \-55.3% |
|    Page |                    1.9 |                            12.3 |               \-52.4% |
|   Cedar |                    1.3 |                             6.9 |               \-50.0% |
|     Ida |                    2.0 |                            29.2 |               \-48.8% |
|    Lyon |                    1.0 |                             8.5 |               \-46.1% |
|  Marion |                    2.7 |                             8.2 |               \-45.8% |
|  Jasper |                    2.9 |                             7.7 |               \-43.8% |
|  Bremer |                    1.6 |                             6.3 |               \-43.8% |
|  Wright |                    0.6 |                             4.5 |               \-42.1% |
