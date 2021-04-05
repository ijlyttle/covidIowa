Compiled at 2021-04-05 00:01:21 UTC

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

## Tables as of 2021-04-04

As of 2021-04-04, IPDH is reporting 430 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  112.1 |                            22.9 |                  5.3% |
|          Linn |                   23.6 |                            10.4 |                 42.1% |
|         Scott |                   60.9 |                            35.2 |                  8.8% |
|       Johnson |                   27.3 |                            18.1 |                 25.3% |
|    Black Hawk |                   16.3 |                            12.4 |                 28.7% |
|      Woodbury |                   31.0 |                            30.1 |                 26.6% |
|       Dubuque |                   23.3 |                            23.9 |                 42.9% |
|         Story |                   24.7 |                            25.4 |                 26.8% |
|        Dallas |                   20.0 |                            21.4 |                  2.8% |
| Pottawattamie |                   30.0 |                            32.2 |                 41.8% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   12.3 |                            71.2 |                  6.9% |
|         Emmet |                    4.9 |                            52.7 |                  5.1% |
|          Clay |                    7.3 |                            45.5 |               \-18.3% |
|     Palo Alto |                    3.4 |                            38.6 |                 29.2% |
|      Plymouth |                    9.4 |                            37.5 |                 28.1% |
|         Scott |                   60.9 |                            35.2 |                  8.8% |
|      Delaware |                    5.7 |                            33.6 |                  9.3% |
|       Guthrie |                    3.6 |                            33.4 |                  3.2% |
| Pottawattamie |                   30.0 |                            32.2 |                 41.8% |
|      Woodbury |                   31.0 |                            30.1 |                 26.6% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Franklin |                    1.6 |                            15.6 |                 79.9% |
|   Hancock |                    2.0 |                            18.8 |                 75.0% |
|    Monroe |                    1.0 |                            13.0 |                 75.0% |
|  Harrison |                    2.7 |                            19.3 |                 73.3% |
| Poweshiek |                    1.1 |                             6.2 |                 66.6% |
|   Clayton |                    1.6 |                             9.0 |                 63.7% |
|     Cedar |                    4.6 |                            24.5 |                 56.0% |
|   Audubon |                    1.1 |                            20.8 |                 50.0% |
|   Dubuque |                   23.3 |                            23.9 |                 42.9% |
|      Linn |                   23.6 |                            10.4 |                 42.1% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Lee |                    2.7 |                             8.1 |               \-70.1% |
|    Shelby |                    1.6 |                            13.7 |               \-48.6% |
|  Ringgold |                    0.3 |                             5.8 |               \-47.1% |
|    Jasper |                    5.1 |                            13.8 |               \-44.2% |
|     Wayne |                    0.6 |                             8.9 |               \-42.1% |
|  Humboldt |                    0.9 |                             9.0 |               \-40.9% |
| Allamakee |                    0.4 |                             3.1 |               \-37.5% |
|  Cherokee |                    1.7 |                            15.3 |               \-36.7% |
|    Greene |                    0.4 |                             4.8 |               \-33.3% |
|   Carroll |                    1.7 |                             8.5 |               \-32.2% |
