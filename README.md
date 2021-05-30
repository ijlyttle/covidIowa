Compiled at 2021-05-30 20:43:07 UTC

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

## Tables as of 2021-05-30

As of 2021-05-30, IPDH is reporting 60 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   14.3 |                             2.9 |               \-51.8% |
|          Linn |                    7.6 |                             3.3 |               \-38.1% |
|         Scott |                    9.9 |                             5.7 |               \-26.2% |
|       Johnson |                    5.1 |                             3.4 |                \-4.4% |
|    Black Hawk |                    6.1 |                             4.7 |                \-9.1% |
|      Woodbury |                    3.0 |                             2.9 |               \-39.1% |
|       Dubuque |                    5.3 |                             5.4 |                 25.7% |
|         Story |                    3.0 |                             3.1 |               \-40.4% |
|        Dallas |                    2.1 |                             2.3 |               \-59.3% |
| Pottawattamie |                    1.0 |                             1.1 |               \-62.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Davis |                    1.1 |                            12.7 |                 15.4% |
|       Adams |                    0.4 |                            11.9 |                  0.0% |
| Cerro Gordo |                    4.7 |                            11.1 |               \-34.4% |
|       Emmet |                    1.0 |                            10.9 |                 75.0% |
|         Ida |                    0.7 |                            10.4 |                 19.9% |
|   Winnebago |                    1.0 |                             9.7 |                 40.0% |
|       Jones |                    1.7 |                             8.3 |                 58.3% |
|   Poweshiek |                    1.3 |                             7.0 |                  6.7% |
|  Des Moines |                    2.6 |                             6.6 |               \-44.5% |
|      Louisa |                    0.7 |                             6.5 |                \-7.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Emmet |                    1.0 |                            10.9 |                 75.0% |
|  Buchanan |                    0.9 |                             4.0 |                 62.5% |
|     Jones |                    1.7 |                             8.3 |                 58.3% |
|    Greene |                    0.4 |                             4.8 |                 42.9% |
| Winnebago |                    1.0 |                             9.7 |                 40.0% |
|      Page |                    0.7 |                             4.7 |                 33.3% |
|  Hamilton |                    0.7 |                             4.8 |                 33.3% |
|    Shelby |                    0.3 |                             2.5 |                 28.6% |
|   Dubuque |                    5.3 |                             5.4 |                 25.7% |
|       Ida |                    0.7 |                            10.4 |                 19.9% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Hancock |                    0.0 |                             0.0 |               \-63.2% |
| Pottawattamie |                    1.0 |                             1.1 |               \-62.2% |
|        Dallas |                    2.1 |                             2.3 |               \-59.3% |
|        Hardin |                    0.0 |                             0.0 |               \-56.3% |
|      Crawford |                    0.1 |                             0.8 |               \-55.5% |
|      Franklin |                    0.4 |                             4.3 |               \-52.4% |
|          Polk |                   14.3 |                             2.9 |               \-51.8% |
|       Clinton |                    1.4 |                             3.1 |               \-50.0% |
|     Allamakee |                    0.0 |                             0.0 |               \-50.0% |
|        Wright |                    0.0 |                             0.0 |               \-50.0% |
