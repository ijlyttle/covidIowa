Compiled at 2021-05-24 00:02:04 UTC

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

## Tables as of 2021-05-23

As of 2021-05-23, IPDH is reporting 115 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   30.7 |                             6.3 |               \-25.0% |
|          Linn |                   12.9 |                             5.7 |               \-27.1% |
|         Scott |                   13.7 |                             7.9 |               \-40.1% |
|       Johnson |                    5.4 |                             3.6 |               \-28.6% |
|    Black Hawk |                    6.9 |                             5.2 |                \-6.8% |
|      Woodbury |                    5.6 |                             5.4 |                  7.0% |
|       Dubuque |                    4.0 |                             4.1 |               \-14.6% |
|         Story |                    5.7 |                             5.9 |                \-9.6% |
|        Dallas |                    6.7 |                             7.2 |                 14.9% |
| Pottawattamie |                    4.3 |                             4.6 |               \-44.8% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    2.0 |                            19.9 |               \-38.2% |
| Cerro Gordo |                    7.7 |                            18.2 |                 45.2% |
|     Hancock |                    1.7 |                            16.1 |                \-9.5% |
|  Des Moines |                    5.4 |                            13.9 |               \-29.7% |
|     Audubon |                    0.7 |                            13.0 |                 19.9% |
|       Adair |                    0.9 |                            12.0 |                 44.4% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|   Palo Alto |                    1.0 |                            11.3 |                 27.3% |
|   Muscatine |                    4.7 |                            11.0 |               \-29.8% |
|     Jackson |                    2.1 |                            11.0 |                 29.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Crawford |                    1.6 |                             9.3 |                 79.9% |
|   Poweshiek |                    1.1 |                             6.2 |                 66.6% |
|  Washington |                    1.4 |                             6.5 |                 54.6% |
| Cerro Gordo |                    7.7 |                            18.2 |                 45.2% |
|       Adair |                    0.9 |                            12.0 |                 44.4% |
|     Fremont |                    0.4 |                             6.2 |                 42.9% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|       Lucas |                    0.6 |                             6.6 |                 37.4% |
|    Marshall |                    2.6 |                             6.5 |                 31.6% |
|     Clayton |                    0.9 |                             4.9 |                 30.0% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|      Buchanan |                    0.1 |                             0.7 |               \-52.9% |
|         Jones |                    0.7 |                             3.5 |               \-52.0% |
|          Cass |                    0.1 |                             1.1 |               \-50.0% |
|        Marion |                    1.1 |                             3.4 |               \-48.3% |
|       Calhoun |                    0.4 |                             4.4 |               \-47.3% |
|      Hamilton |                    0.3 |                             1.9 |               \-47.1% |
|      Mitchell |                    0.0 |                             0.0 |               \-46.1% |
|       Osceola |                    0.0 |                             0.0 |               \-46.1% |
| Pottawattamie |                    4.3 |                             4.6 |               \-44.8% |
|     Winnebago |                    0.4 |                             4.1 |               \-41.2% |
