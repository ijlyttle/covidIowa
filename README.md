Compiled at 2021-04-26 20:20:05 UTC

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

## Tables as of 2021-04-26

As of 2021-04-26, IPDH is reporting 182 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   81.4 |                            16.6 |                 11.4% |
|          Linn |                   24.4 |                            10.8 |                  9.2% |
|         Scott |                   37.6 |                            21.7 |               \-33.5% |
|       Johnson |                   25.0 |                            16.5 |               \-10.3% |
|    Black Hawk |                   12.4 |                             9.5 |                \-9.6% |
|      Woodbury |                   14.1 |                            13.7 |               \-16.5% |
|       Dubuque |                   10.1 |                            10.4 |               \-45.1% |
|         Story |                   13.6 |                            14.0 |                 32.5% |
|        Dallas |                   14.7 |                            15.7 |                 29.4% |
| Pottawattamie |                   18.4 |                            19.8 |                \-8.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    2.4 |                            40.8 |                \-7.7% |
|     Emmet |                    3.4 |                            37.2 |                 34.8% |
| Winnebago |                    3.4 |                            33.1 |                106.7% |
| Dickinson |                    4.1 |                            24.0 |               \-16.3% |
|    Warren |                   12.3 |                            23.9 |                 13.4% |
|     Floyd |                    3.7 |                            23.7 |                106.2% |
|       Sac |                    2.3 |                            23.5 |                  0.0% |
|     Scott |                   37.6 |                            21.7 |               \-33.5% |
|     Worth |                    1.6 |                            21.3 |                 20.0% |
|  Delaware |                    3.6 |                            21.0 |                  6.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Marion |                    3.6 |                            10.7 |                146.1% |
|      Lucas |                    1.6 |                            18.3 |                124.9% |
|  Winnebago |                    3.4 |                            33.1 |                106.7% |
|      Floyd |                    3.7 |                            23.7 |                106.2% |
|     Jasper |                    4.0 |                            10.8 |                 94.5% |
|    Carroll |                    4.1 |                            20.5 |                 89.5% |
|   Franklin |                    1.9 |                            18.4 |                 81.9% |
|  Allamakee |                    0.7 |                             5.2 |                 71.4% |
| Des Moines |                    6.6 |                            16.9 |                 70.9% |
|     Howard |                    1.1 |                            12.5 |                 66.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-0.9 |                           \-7.0 |               \-90.9% |
| Winneshiek |                    0.9 |                             4.3 |               \-53.6% |
|     Shelby |                    0.9 |                             7.5 |               \-51.9% |
|   Buchanan |                    0.7 |                             3.4 |               \-47.8% |
|   Plymouth |                    2.3 |                             9.1 |               \-46.5% |
|    Clayton |                    0.9 |                             4.9 |               \-45.8% |
|    Dubuque |                   10.1 |                            10.4 |               \-45.1% |
|       Page |                    0.7 |                             4.7 |               \-42.9% |
|     Grundy |                    0.1 |                             1.2 |               \-42.8% |
|  Palo Alto |                    0.9 |                             9.6 |               \-38.1% |
