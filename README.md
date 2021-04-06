Compiled at 2021-04-06 00:03:10 UTC

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

## Tables as of 2021-04-05

As of 2021-04-05, IPDH is reporting 152 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   91.1 |                            18.6 |               \-22.6% |
|          Linn |                   21.3 |                             9.4 |                 28.9% |
|         Scott |                   57.6 |                            33.3 |                \-1.4% |
|       Johnson |                   26.7 |                            17.7 |                 17.6% |
|    Black Hawk |                   13.0 |                             9.9 |               \-11.7% |
|      Woodbury |                   27.0 |                            26.2 |                \-6.2% |
|       Dubuque |                   23.1 |                            23.8 |                 32.0% |
|         Story |                   23.0 |                            23.7 |                 13.5% |
|        Dallas |                   14.4 |                            15.4 |               \-37.2% |
| Pottawattamie |                   28.3 |                            30.3 |                 26.5% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   11.6 |                            67.0 |                \-1.1% |
|         Emmet |                    4.3 |                            46.5 |               \-15.9% |
|          Clay |                    6.4 |                            40.1 |               \-26.8% |
|      Plymouth |                    9.6 |                            38.0 |                 34.5% |
|     Palo Alto |                    3.1 |                            35.4 |                  7.4% |
|      Delaware |                    5.9 |                            34.4 |                 20.0% |
|         Scott |                   57.6 |                            33.3 |                \-1.4% |
| Pottawattamie |                   28.3 |                            30.3 |                 26.5% |
|       Guthrie |                    3.1 |                            29.4 |               \-14.7% |
|      Woodbury |                   27.0 |                            26.2 |                \-6.2% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Monroe |                    1.0 |                            13.0 |                 75.0% |
|   Audubon |                    1.1 |                            20.8 |                 66.6% |
| Chickasaw |                    0.7 |                             6.0 |                 50.0% |
|  Harrison |                    2.4 |                            17.3 |                 41.2% |
|     Cedar |                    4.1 |                            22.2 |                 38.5% |
|  Crawford |                    1.6 |                             9.3 |                 38.4% |
|  Plymouth |                    9.6 |                            38.0 |                 34.5% |
|  Buchanan |                    3.6 |                            16.9 |                 33.3% |
|   Dubuque |                   23.1 |                            23.8 |                 32.0% |
|      Linn |                   21.3 |                             9.4 |                 28.9% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Lee |                    2.7 |                             8.1 |               \-70.1% |
|   Jasper |                    3.9 |                            10.4 |               \-60.9% |
|   Shelby |                    1.4 |                            12.5 |               \-51.4% |
|    Wayne |                    0.3 |                             4.4 |               \-47.1% |
| Ringgold |                    0.3 |                             5.8 |               \-47.1% |
| Cherokee |                    1.4 |                            12.7 |               \-46.9% |
|  Osceola |                    1.3 |                            21.6 |               \-42.8% |
| Mitchell |                    0.7 |                             6.7 |               \-40.0% |
|    Mills |                    1.3 |                             8.5 |               \-38.4% |
| Humboldt |                    0.9 |                             9.0 |               \-38.1% |
