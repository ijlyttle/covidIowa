Compiled at 2021-05-25 00:02:25 UTC

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

## Tables as of 2021-05-24

As of 2021-05-24, IPDH is reporting 55 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   29.9 |                             6.1 |               \-23.4% |
|          Linn |                   11.1 |                             4.9 |               \-39.7% |
|         Scott |                   12.7 |                             7.4 |               \-45.5% |
|       Johnson |                    5.3 |                             3.5 |               \-29.0% |
|    Black Hawk |                    7.4 |                             5.7 |                  3.5% |
|      Woodbury |                    4.7 |                             4.6 |               \-21.6% |
|       Dubuque |                    4.6 |                             4.7 |                \-7.2% |
|         Story |                    5.1 |                             5.3 |               \-20.4% |
|        Dallas |                    6.3 |                             6.7 |                  6.3% |
| Pottawattamie |                    4.0 |                             4.3 |               \-47.8% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    2.0 |                            19.9 |               \-34.4% |
| Cerro Gordo |                    7.3 |                            17.2 |                 34.9% |
|  Des Moines |                    5.4 |                            13.9 |               \-25.0% |
|     Hancock |                    1.4 |                            13.4 |               \-22.7% |
|     Audubon |                    0.7 |                            13.0 |                 19.9% |
|       Adair |                    0.9 |                            12.0 |                 44.4% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|     Jackson |                    2.3 |                            11.8 |                 35.3% |
|   Palo Alto |                    1.0 |                            11.3 |                 27.3% |
|       Henry |                    2.1 |                            10.7 |                 22.2% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|   Poweshiek |                    1.1 |                             6.2 |                 66.6% |
|      Louisa |                    1.0 |                             9.1 |                 55.5% |
|      Hardin |                    1.6 |                             9.3 |                 50.0% |
|       Adair |                    0.9 |                            12.0 |                 44.4% |
|     Fremont |                    0.4 |                             6.2 |                 42.9% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|       Lucas |                    0.6 |                             6.6 |                 37.4% |
|    Crawford |                    1.1 |                             6.8 |                 36.4% |
|     Jackson |                    2.3 |                            11.8 |                 35.3% |
| Cerro Gordo |                    7.3 |                            17.2 |                 34.9% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Calhoun |                    0.3 |                             3.0 |               \-55.0% |
|      Buchanan |                    0.1 |                             0.7 |               \-52.9% |
| Pottawattamie |                    4.0 |                             4.3 |               \-47.8% |
|         Jones |                    0.7 |                             3.5 |               \-47.8% |
|       Osceola |                    0.0 |                             0.0 |               \-46.1% |
|         Scott |                   12.7 |                             7.4 |               \-45.5% |
|      Hamilton |                    0.3 |                             1.9 |               \-43.7% |
|     Muscatine |                    4.1 |                             9.7 |               \-42.9% |
|          Cass |                    0.1 |                             1.1 |               \-42.8% |
|     Winnebago |                    0.4 |                             4.1 |               \-41.2% |
