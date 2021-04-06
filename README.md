Compiled at 2021-04-06 20:23:37 UTC

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

## Tables as of 2021-04-06

As of 2021-04-06, IPDH is reporting 507 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  101.6 |                            20.7 |               \-11.1% |
|          Linn |                   24.4 |                            10.8 |                 58.9% |
|         Scott |                   63.1 |                            36.5 |                 12.0% |
|       Johnson |                   30.6 |                            20.2 |                 46.4% |
|    Black Hawk |                   14.7 |                            11.2 |                  2.8% |
|      Woodbury |                   29.6 |                            28.7 |                  7.0% |
|       Dubuque |                   27.3 |                            28.0 |                 62.3% |
|         Story |                   25.1 |                            25.9 |                 25.3% |
|        Dallas |                   16.6 |                            17.7 |               \-27.6% |
| Pottawattamie |                   30.1 |                            32.3 |                 37.1% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   12.7 |                            73.7 |                  7.9% |
|         Emmet |                    4.7 |                            51.2 |                \-9.1% |
|          Clay |                    8.1 |                            50.8 |                \-7.2% |
|      Plymouth |                   12.1 |                            48.2 |                 73.6% |
|      Delaware |                    6.9 |                            40.3 |                 41.0% |
|     Palo Alto |                    3.3 |                            37.0 |                 15.4% |
|         Scott |                   63.1 |                            36.5 |                 12.0% |
|       Osceola |                    2.0 |                            33.6 |               \-25.0% |
| Pottawattamie |                   30.1 |                            32.3 |                 37.1% |
|       Guthrie |                    3.4 |                            32.1 |                \-6.0% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Carroll |                    5.7 |                            28.3 |                 95.8% |
|   Monroe |                    1.0 |                            13.0 |                 75.0% |
| Plymouth |                   12.1 |                            48.2 |                 73.6% |
|  Clayton |                    2.1 |                            12.2 |                 69.3% |
| Harrison |                    2.6 |                            18.3 |                 66.6% |
|    Cedar |                    4.9 |                            26.1 |                 64.0% |
|  Dubuque |                   27.3 |                            28.0 |                 62.3% |
|    Worth |                    1.3 |                            17.4 |                 60.0% |
|     Linn |                   24.4 |                            10.8 |                 58.9% |
| Crawford |                    2.3 |                            13.6 |                 53.3% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Lee |                    2.9 |                             8.5 |               \-69.0% |
|   Jasper |                    4.0 |                            10.8 |               \-58.8% |
|   Shelby |                    1.6 |                            13.7 |               \-48.6% |
|    Wayne |                    0.4 |                             6.7 |               \-41.2% |
| Mitchell |                    0.7 |                             6.7 |               \-40.0% |
| Cherokee |                    1.9 |                            16.5 |               \-37.5% |
| Ringgold |                    0.6 |                            11.7 |               \-35.3% |
| Humboldt |                    0.9 |                             9.0 |               \-35.0% |
|    Mills |                    1.6 |                            10.4 |               \-30.8% |
|   Dallas |                   16.6 |                            17.7 |               \-27.6% |
