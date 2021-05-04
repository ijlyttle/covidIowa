Compiled at 2021-05-04 23:58:41 UTC

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

## Tables as of 2021-05-04

As of 2021-05-04, IPDH is reporting 373 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   62.3 |                            12.7 |               \-17.2% |
|          Linn |                   21.3 |                             9.4 |                \-9.3% |
|         Scott |                   41.0 |                            23.7 |                 17.1% |
|       Johnson |                   17.1 |                            11.3 |               \-17.0% |
|    Black Hawk |                   10.4 |                             7.9 |                \-4.8% |
|      Woodbury |                    8.4 |                             8.2 |               \-32.0% |
|       Dubuque |                    8.1 |                             8.4 |                \-8.6% |
|         Story |                   14.7 |                            15.2 |                 14.6% |
|        Dallas |                   11.1 |                            11.9 |               \-13.3% |
| Pottawattamie |                   15.9 |                            17.0 |                \-8.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.4 |                            44.4 |                349.9% |
|   Madison |                    5.0 |                            30.6 |                 61.6% |
|  Franklin |                    2.6 |                            25.5 |                 13.6% |
|     Worth |                    1.9 |                            25.2 |                 25.0% |
|     Emmet |                    2.3 |                            24.8 |               \-14.8% |
|     Scott |                   41.0 |                            23.7 |                 17.1% |
| Winnebago |                    2.3 |                            22.1 |               \-25.8% |
|   Hancock |                    2.3 |                            21.5 |                 27.8% |
|  Ringgold |                    1.0 |                            20.4 |                 75.0% |
|     Adams |                    0.7 |                            19.8 |                 50.0% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.4 |                            44.4 |                349.9% |
|    Shelby |                    1.7 |                            15.0 |                 89.9% |
|   Calhoun |                    1.9 |                            19.2 |                 81.9% |
|  Ringgold |                    1.0 |                            20.4 |                 75.0% |
|   Mahaska |                    3.3 |                            14.9 |                 66.7% |
|   Madison |                    5.0 |                            30.6 |                 61.6% |
|    Grundy |                    0.6 |                             4.7 |                 57.1% |
| Allamakee |                    1.0 |                             7.3 |                 55.5% |
| Chickasaw |                    1.0 |                             8.4 |                 55.5% |
|   Decatur |                    1.0 |                            12.7 |                 55.5% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Floyd |                    1.1 |                             7.3 |               \-55.9% |
|     Osceola |                    0.3 |                             4.8 |               \-52.6% |
|        Clay |                    1.0 |                             6.2 |               \-41.7% |
|     Kossuth |                    0.4 |                             2.9 |               \-41.2% |
|  Montgomery |                    0.7 |                             7.2 |               \-40.0% |
| Cerro Gordo |                    5.4 |                            12.8 |               \-38.4% |
|     Jackson |                    0.9 |                             4.4 |               \-38.1% |
|         Sac |                    0.9 |                             8.8 |               \-35.0% |
| Buena Vista |                    1.0 |                             5.1 |               \-33.3% |
|   Jefferson |                    0.4 |                             2.3 |               \-33.3% |
