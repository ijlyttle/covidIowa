Compiled at 2021-08-11 17:31:56 UTC

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

## Tables as of 2021-08-04

As of 2021-08-04, IPDH is reporting 3570 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  141.6 |                            28.9 |                607.8% |
|          Linn |                   55.6 |                            24.5 |                800.0% |
|         Scott |                   44.1 |                            25.5 |                485.2% |
|       Johnson |                   29.3 |                            19.4 |                583.8% |
|    Black Hawk |                   76.1 |                            58.0 |                318.6% |
|      Woodbury |                   34.9 |                            33.8 |                457.7% |
|       Dubuque |                   13.0 |                            13.4 |                345.4% |
|         Story |                   32.4 |                            33.4 |                800.1% |
|        Dallas |                   30.3 |                            32.4 |                584.4% |
| Pottawattamie |                   32.0 |                            34.3 |                669.9% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   37.3 |                           110.8 |                892.6% |
|    Webster |                   34.3 |                            95.5 |                197.6% |
|        Ida |                    5.4 |                            79.1 |                542.9% |
| Des Moines |                   27.1 |                            69.7 |                347.7% |
|     Monroe |                    5.0 |                            64.9 |                147.0% |
|   Humboldt |                    6.0 |                            62.8 |                188.2% |
|   Hamilton |                    9.1 |                            61.9 |                184.0% |
|     Wright |                    7.7 |                            61.4 |                154.1% |
|   Franklin |                    6.1 |                            61.0 |                150.0% |
|    Kossuth |                    8.7 |                            58.8 |                353.3% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|           Lee |                   37.3 |                           110.8 |                892.6% |
|         Story |                   32.4 |                            33.4 |                800.1% |
|          Linn |                   55.6 |                            24.5 |                800.0% |
|     Muscatine |                   12.7 |                            29.8 |                700.1% |
| Pottawattamie |                   32.0 |                            34.3 |                669.9% |
|          Polk |                  141.6 |                            28.9 |                607.8% |
|        Dallas |                   30.3 |                            32.4 |                584.4% |
|       Johnson |                   29.3 |                            19.4 |                583.8% |
|        Jasper |                   12.9 |                            34.6 |                546.6% |
|           Ida |                    5.4 |                            79.1 |                542.9% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Mitchell |                    0.1 |                             1.4 |               \-38.4% |
| Montgomery |                    1.4 |                            14.4 |                  6.3% |
|     Monona |                    1.9 |                            21.6 |                 17.6% |
|     Taylor |                    0.3 |                             4.7 |                 28.6% |
|    Fremont |                    0.7 |                            10.3 |                 33.3% |
|     Shelby |                    2.3 |                            20.0 |                 43.7% |
|      Union |                    0.9 |                             7.0 |                 44.4% |
|    Decatur |                    2.6 |                            32.7 |                 47.0% |
|    Hancock |                    3.7 |                            34.9 |                 50.0% |
|     Keokuk |                    1.6 |                            15.3 |                 50.0% |
