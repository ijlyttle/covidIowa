Compiled at 2021-04-25 17:13:22 UTC

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

## Tables as of 2021-04-25

As of 2021-04-25, IPDH is reporting 220 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   78.9 |                            16.1 |                  6.5% |
|          Linn |                   26.0 |                            11.5 |                 23.5% |
|         Scott |                   38.3 |                            22.1 |               \-33.6% |
|       Johnson |                   24.9 |                            16.4 |               \-10.8% |
|    Black Hawk |                   12.3 |                             9.4 |               \-13.9% |
|      Woodbury |                   14.0 |                            13.6 |               \-19.8% |
|       Dubuque |                   10.1 |                            10.4 |               \-46.2% |
|         Story |                   13.0 |                            13.4 |                 32.4% |
|        Dallas |                   14.1 |                            15.1 |                 24.7% |
| Pottawattamie |                   19.6 |                            21.0 |                \-1.4% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    2.7 |                            45.6 |                  4.0% |
|     Emmet |                    3.6 |                            38.8 |                 33.3% |
| Winnebago |                    3.3 |                            31.7 |                100.0% |
|       Sac |                    2.4 |                            25.0 |                  9.1% |
| Dickinson |                    4.1 |                            24.0 |               \-16.3% |
|     Worth |                    1.7 |                            23.2 |                 26.6% |
|    Warren |                   11.7 |                            22.8 |                 11.2% |
|     Scott |                   38.3 |                            22.1 |               \-33.6% |
|     Floyd |                    3.4 |                            21.9 |                 82.3% |
|    Hardin |                    3.6 |                            21.2 |                 45.4% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Lucas |                    1.6 |                            18.3 |                124.9% |
|    Marion |                    3.1 |                             9.5 |                123.1% |
| Winnebago |                    3.3 |                            31.7 |                100.0% |
|  Franklin |                    1.9 |                            18.4 |                 99.9% |
|     Henry |                    3.1 |                            15.8 |                 93.3% |
|     Floyd |                    3.4 |                            21.9 |                 82.3% |
|      Tama |                    1.6 |                             9.3 |                 79.9% |
|   Carroll |                    3.7 |                            18.4 |                 73.7% |
| Allamakee |                    0.7 |                             5.2 |                 71.4% |
|      Cass |                    2.4 |                            18.9 |                 71.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-0.9 |                           \-7.0 |               \-90.9% |
|     Shelby |                    0.9 |                             7.5 |               \-53.6% |
|        Ida |                    0.3 |                             4.2 |               \-52.6% |
|    Clayton |                    0.7 |                             4.1 |               \-50.0% |
|    Dubuque |                   10.1 |                            10.4 |               \-46.2% |
| Winneshiek |                    1.1 |                             5.7 |               \-44.4% |
|     Wright |                    1.0 |                             8.0 |               \-44.0% |
|       Page |                    0.7 |                             4.7 |               \-42.9% |
|     Grundy |                    0.1 |                             1.2 |               \-42.8% |
|   Buchanan |                    0.9 |                             4.0 |               \-40.9% |
