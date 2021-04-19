Compiled at 2021-04-19 17:11:34 UTC

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

## Tables as of 2021-04-19

As of 2021-04-19, IPDH is reporting 168 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   73.0 |                            14.9 |               \-18.6% |
|          Linn |                   22.3 |                             9.8 |               \-16.4% |
|         Scott |                   57.0 |                            33.0 |                \-3.1% |
|       Johnson |                   28.0 |                            18.5 |                \-1.9% |
|    Black Hawk |                   13.9 |                            10.6 |               \-20.6% |
|      Woodbury |                   17.1 |                            16.6 |               \-17.5% |
|       Dubuque |                   19.3 |                            19.8 |               \-28.6% |
|         Story |                   10.0 |                            10.3 |               \-26.7% |
|        Dallas |                   11.1 |                            11.9 |               \-15.8% |
| Pottawattamie |                   20.3 |                            21.8 |               \-15.8% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    2.7 |                            45.6 |                  8.3% |
|         Scott |                   57.0 |                            33.0 |                \-3.1% |
|     Dickinson |                    5.1 |                            29.8 |               \-37.7% |
|          Clay |                    4.1 |                            25.9 |               \-29.4% |
|        Shelby |                    2.9 |                            24.9 |               \-10.0% |
|         Emmet |                    2.3 |                            24.8 |               \-20.7% |
|           Sac |                    2.3 |                            23.5 |                 43.7% |
|     Palo Alto |                    2.0 |                            22.5 |                \-4.5% |
| Pottawattamie |                   20.3 |                            21.8 |               \-15.8% |
|     Muscatine |                    9.0 |                            21.1 |                  4.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Monona |                    1.3 |                            14.9 |                100.0% |
| Pocahontas |                    1.0 |                            15.1 |                100.0% |
|    Madison |                    3.1 |                            19.2 |                 93.3% |
|  Appanoose |                    1.1 |                             9.2 |                 87.5% |
|     Benton |                    2.0 |                             7.8 |                 61.6% |
|    Webster |                    3.1 |                             8.8 |                 61.1% |
|    Guthrie |                    1.7 |                            16.0 |                 46.1% |
|        Sac |                    2.3 |                            23.5 |                 43.7% |
|   Hamilton |                    1.6 |                            10.6 |                 38.4% |
|      Adair |                    0.7 |                            10.0 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                    1.7 |                             8.5 |               \-55.8% |
|      Marion |                    0.9 |                             2.6 |               \-51.9% |
|     Wapello |                    1.1 |                             3.3 |               \-44.4% |
|    Cherokee |                    1.0 |                             8.9 |               \-39.1% |
|       Davis |                    0.1 |                             1.6 |               \-38.4% |
|        Page |                    2.0 |                            13.2 |               \-38.2% |
|    Crawford |                    0.9 |                             5.1 |               \-38.1% |
|   Dickinson |                    5.1 |                            29.8 |               \-37.7% |
|       Union |                    0.6 |                             4.7 |               \-35.3% |
| Buena Vista |                    1.1 |                             5.8 |               \-34.8% |
