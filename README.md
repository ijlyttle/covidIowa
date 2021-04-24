Compiled at 2021-04-24 20:20:11 UTC

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

## Tables as of 2021-04-24

As of 2021-04-24, IPDH is reporting 436 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   89.1 |                            18.2 |                 29.6% |
|          Linn |                   29.4 |                            13.0 |                 36.5% |
|         Scott |                   47.0 |                            27.2 |                \-9.7% |
|       Johnson |                   29.0 |                            19.2 |                  6.1% |
|    Black Hawk |                   15.7 |                            12.0 |                 27.2% |
|      Woodbury |                   16.7 |                            16.2 |                  1.6% |
|       Dubuque |                   14.3 |                            14.7 |               \-18.9% |
|         Story |                   14.4 |                            14.9 |                 50.0% |
|        Dallas |                   15.0 |                            16.1 |                 36.6% |
| Pottawattamie |                   23.3 |                            25.0 |                 25.9% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    3.3 |                            55.2 |                 36.4% |
|         Emmet |                    3.7 |                            40.3 |                 65.0% |
|     Winnebago |                    3.4 |                            33.1 |                158.4% |
|     Dickinson |                    5.1 |                            29.8 |                 16.2% |
|           Sac |                    2.7 |                            27.9 |                 23.8% |
|         Scott |                   47.0 |                            27.2 |                \-9.7% |
|          Clay |                    4.3 |                            26.8 |                 15.6% |
|      Delaware |                    4.3 |                            25.2 |                 54.2% |
| Pottawattamie |                   23.3 |                            25.0 |                 25.9% |
|        Warren |                   12.7 |                            24.7 |                 26.3% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|   Winnebago |                    3.4 |                            33.1 |                158.4% |
|   Jefferson |                    1.6 |                             8.6 |                157.1% |
|      Marion |                    3.1 |                             9.5 |                141.7% |
|        Cass |                    2.7 |                            21.1 |                136.4% |
|       Henry |                    3.3 |                            16.5 |                130.8% |
|       Lucas |                    1.6 |                            18.3 |                124.9% |
|  Des Moines |                    7.7 |                            19.8 |                103.3% |
|    Franklin |                    1.6 |                            15.6 |                 99.9% |
|  Montgomery |                    2.3 |                            23.1 |                 91.7% |
| Cerro Gordo |                    8.4 |                            19.9 |                 88.6% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                  \-0.9 |                           \-7.0 |               \-90.0% |
|   Clayton |                    1.0 |                             5.7 |               \-39.1% |
|      Page |                    0.9 |                             5.7 |               \-35.0% |
|  Hamilton |                    0.9 |                             5.8 |               \-35.0% |
| Van Buren |                    0.0 |                             0.0 |               \-30.0% |
|  Ringgold |                    0.0 |                             0.0 |               \-30.0% |
|    Butler |                    0.4 |                             3.0 |               \-28.6% |
| Chickasaw |                    0.4 |                             3.6 |               \-28.6% |
|    Wright |                    1.3 |                            10.2 |               \-27.3% |
|     Wayne |                    0.1 |                             2.2 |               \-27.2% |
