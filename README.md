Compiled at 2021-05-22 17:12:48 UTC

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

## Tables as of 2021-05-22

As of 2021-05-22, IPDH is reporting 170 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   32.3 |                             6.6 |               \-19.4% |
|          Linn |                   13.1 |                             5.8 |               \-21.4% |
|         Scott |                   15.0 |                             8.7 |               \-39.1% |
|       Johnson |                    5.4 |                             3.6 |               \-25.0% |
|    Black Hawk |                    6.6 |                             5.0 |               \-10.2% |
|      Woodbury |                    5.6 |                             5.4 |                  9.5% |
|       Dubuque |                    3.9 |                             4.0 |               \-17.1% |
|         Story |                    5.3 |                             5.4 |               \-20.0% |
|        Dallas |                    7.1 |                             7.6 |                  1.8% |
| Pottawattamie |                    4.9 |                             5.2 |               \-41.4% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    1.9 |                            18.4 |               \-46.0% |
| Cerro Gordo |                    7.7 |                            18.2 |                 38.6% |
|       Davis |                    1.6 |                            17.5 |                 28.6% |
|  Des Moines |                    6.0 |                            15.4 |               \-15.5% |
|     Hancock |                    1.6 |                            14.8 |               \-14.3% |
|     Audubon |                    0.7 |                            13.0 |                 19.9% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|   Palo Alto |                    1.0 |                            11.3 |                 16.7% |
|   Muscatine |                    4.7 |                            11.0 |               \-34.4% |
|     Jackson |                    2.1 |                            11.0 |                 22.2% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|   Jefferson |                    0.9 |                             4.7 |                 85.7% |
|   Appanoose |                    0.7 |                             5.7 |                 71.4% |
|   Poweshiek |                    1.1 |                             6.2 |                 66.6% |
|  Washington |                    1.4 |                             6.5 |                 54.6% |
|    Crawford |                    1.1 |                             6.8 |                 50.0% |
|     Fremont |                    0.4 |                             6.2 |                 42.9% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
| Cerro Gordo |                    7.7 |                            18.2 |                 38.6% |
|       Lucas |                    0.6 |                             6.6 |                 37.4% |
|      Louisa |                    0.7 |                             6.5 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|         Jones |                    0.7 |                             3.5 |               \-50.0% |
|      Mitchell |                    0.0 |                             0.0 |               \-46.1% |
|      Franklin |                    1.9 |                            18.4 |               \-46.0% |
|        Warren |                    2.1 |                             4.2 |               \-45.0% |
|      Buchanan |                    0.3 |                             1.4 |               \-43.7% |
|       Osceola |                    0.1 |                             2.4 |               \-42.8% |
| Pottawattamie |                    4.9 |                             5.2 |               \-41.4% |
|        Jasper |                    1.1 |                             3.1 |               \-40.0% |
|     Dickinson |                    0.3 |                             1.7 |               \-40.0% |
|         Scott |                   15.0 |                             8.7 |               \-39.1% |
