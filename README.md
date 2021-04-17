Compiled at 2021-04-17 17:08:11 UTC

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

## Tables as of 2021-04-17

As of 2021-04-17, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |
| 2021-04-13 |                  511.9 |                            16.2 |               \-14.0% |
| 2021-04-12 |                  520.7 |                            16.5 |                \-0.4% |
| 2021-04-11 |                  521.6 |                            16.5 |               \-11.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   68.6 |                            14.0 |               \-22.5% |
|          Linn |                   21.3 |                             9.4 |               \-11.9% |
|         Scott |                   52.1 |                            30.1 |               \-10.6% |
|       Johnson |                   27.3 |                            18.1 |                  0.0% |
|    Black Hawk |                   12.1 |                             9.3 |               \-27.0% |
|      Woodbury |                   16.4 |                            15.9 |               \-23.3% |
|       Dubuque |                   17.9 |                            18.4 |               \-33.7% |
|         Story |                    9.3 |                             9.6 |               \-33.9% |
|        Dallas |                   10.7 |                            11.5 |               \-20.4% |
| Pottawattamie |                   18.3 |                            19.6 |               \-25.0% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    2.1 |                            36.0 |                  0.0% |
|     Scott |                   52.1 |                            30.1 |               \-10.6% |
| Dickinson |                    4.3 |                            24.8 |               \-47.9% |
|      Clay |                    3.6 |                            22.3 |               \-30.4% |
|     Worth |                    1.6 |                            21.3 |               \-10.0% |
| Palo Alto |                    1.9 |                            20.9 |                \-9.1% |
|       Ida |                    1.4 |                            20.8 |                 21.5% |
|       Sac |                    2.0 |                            20.6 |                 16.7% |
|     Emmet |                    1.9 |                            20.2 |               \-35.5% |
|   Clinton |                    9.1 |                            19.7 |                \-9.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Hamilton |                    1.9 |                            12.6 |                 99.9% |
| Pocahontas |                    0.6 |                             8.6 |                 57.1% |
|  Appanoose |                    1.0 |                             8.0 |                 55.5% |
|    Madison |                    2.7 |                            16.6 |                 44.5% |
|   Humboldt |                    0.6 |                             6.0 |                 37.4% |
|    Guthrie |                    1.6 |                            14.7 |                 28.6% |
|  Chickasaw |                    1.0 |                             8.4 |                 27.3% |
|      Adair |                    0.6 |                             8.0 |                 22.2% |
|      Wayne |                    0.6 |                             8.9 |                 22.2% |
|     Benton |                    1.4 |                             5.6 |                 21.5% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Marion |                    0.7 |                             2.1 |               \-60.0% |
|       Davis |                    0.1 |                             1.6 |               \-52.9% |
|    Delaware |                    2.4 |                            14.3 |               \-50.0% |
|      Shelby |                    1.3 |                            11.2 |               \-50.0% |
|   Dickinson |                    4.3 |                            24.8 |               \-47.9% |
|    Cherokee |                    0.7 |                             6.4 |               \-47.8% |
| Cerro Gordo |                    4.0 |                             9.4 |               \-47.0% |
|    Marshall |                    1.0 |                             2.5 |               \-46.1% |
|     Carroll |                    2.0 |                             9.9 |               \-46.1% |
|    Harrison |                    1.6 |                            11.2 |               \-43.8% |
