Compiled at 2021-04-30 23:59:43 UTC

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

## Tables as of 2021-04-30

As of 2021-04-30, IPDH is reporting 372 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   62.1 |                            12.7 |               \-21.2% |
|          Linn |                   23.3 |                            10.3 |                \-5.0% |
|         Scott |                   37.3 |                            21.6 |               \-10.1% |
|       Johnson |                   19.1 |                            12.7 |               \-27.7% |
|    Black Hawk |                    9.9 |                             7.5 |               \-26.9% |
|      Woodbury |                    8.1 |                             7.9 |               \-42.9% |
|       Dubuque |                    7.9 |                             8.1 |               \-39.8% |
|         Story |                   14.1 |                            14.6 |                 17.8% |
|        Dallas |                   11.3 |                            12.1 |                \-8.5% |
| Pottawattamie |                   15.0 |                            16.1 |               \-21.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|   Winnebago |                    3.3 |                            31.7 |                 25.0% |
|       Worth |                    2.3 |                            31.0 |                 53.3% |
|       Union |                    3.4 |                            28.0 |                   Inf |
|       Emmet |                    2.6 |                            27.9 |               \-10.7% |
|    Franklin |                    2.6 |                            25.5 |                 56.2% |
|     Hancock |                    2.6 |                            24.2 |                 56.2% |
|       Adams |                    0.9 |                            23.8 |                 30.0% |
| Cerro Gordo |                    9.4 |                            22.2 |                 30.4% |
|       Adair |                    1.6 |                            22.0 |                 50.0% |
|       Scott |                   37.3 |                            21.6 |               \-10.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    3.4 |                            28.0 |                   Inf |
|   Calhoun |                    1.9 |                            19.2 |                 99.9% |
|    Jasper |                    4.4 |                            11.9 |                 90.0% |
|    Howard |                    1.4 |                            15.6 |                 88.9% |
|     Wayne |                    0.9 |                            13.3 |                 85.7% |
|  Marshall |                    3.0 |                             7.6 |                 75.0% |
| Appanoose |                    1.1 |                             9.2 |                 66.6% |
|  Ringgold |                    0.6 |                            11.7 |                 57.1% |
|   Hancock |                    2.6 |                            24.2 |                 56.2% |
|  Franklin |                    2.6 |                            25.5 |                 56.2% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    0.3 |                             4.8 |               \-70.0% |
|  Plymouth |                    0.4 |                             1.7 |               \-65.5% |
|    Shelby |                    0.4 |                             3.7 |               \-58.3% |
|       Sac |                    0.7 |                             7.3 |               \-53.9% |
|     Sioux |                    1.9 |                             5.3 |               \-50.0% |
|     Boone |                    1.0 |                             3.8 |               \-50.0% |
|   Kossuth |                    0.6 |                             3.9 |               \-47.6% |
| Palo Alto |                    0.3 |                             3.2 |               \-43.7% |
|  Woodbury |                    8.1 |                             7.9 |               \-42.9% |
|    Keokuk |                    0.1 |                             1.4 |               \-42.8% |
