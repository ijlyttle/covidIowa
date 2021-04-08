Compiled at 2021-04-08 00:02:52 UTC

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

## Tables as of 2021-04-07

As of 2021-04-07, IPDH is reporting 759 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   92.9 |                            18.9 |               \-25.8% |
|          Linn |                   23.1 |                            10.2 |                 24.3% |
|         Scott |                   63.7 |                            36.8 |                \-1.1% |
|       Johnson |                   26.9 |                            17.8 |                \-0.5% |
|    Black Hawk |                   14.7 |                            11.2 |               \-11.3% |
|      Woodbury |                   22.7 |                            22.0 |               \-32.0% |
|       Dubuque |                   29.3 |                            30.1 |                 43.2% |
|         Story |                   18.9 |                            19.4 |               \-29.4% |
|        Dallas |                   13.7 |                            14.7 |               \-45.2% |
| Pottawattamie |                   28.7 |                            30.8 |                 11.8% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   13.4 |                            77.8 |                  6.3% |
|         Emmet |                    4.6 |                            49.6 |               \-17.0% |
|          Clay |                    7.3 |                            45.5 |               \-19.4% |
|      Plymouth |                   10.4 |                            41.4 |                 19.4% |
|         Scott |                   63.7 |                            36.8 |                \-1.1% |
|     Palo Alto |                    3.0 |                            33.8 |               \-15.1% |
|      Delaware |                    5.6 |                            32.7 |                \-2.1% |
|           Sac |                    3.1 |                            32.3 |                 45.0% |
| Pottawattamie |                   28.7 |                            30.8 |                 11.8% |
|       Dubuque |                   29.3 |                            30.1 |                 43.2% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Harrison |                    2.7 |                            19.3 |                100.0% |
|     Carroll |                    5.3 |                            26.2 |                 91.3% |
|       Worth |                    1.7 |                            23.2 |                 89.9% |
|    Crawford |                    2.4 |                            14.4 |                 84.7% |
|         Sac |                    3.1 |                            32.3 |                 45.0% |
|     Dubuque |                   29.3 |                            30.1 |                 43.2% |
| Buena Vista |                    2.7 |                            13.8 |                 36.8% |
|        Tama |                    1.1 |                             6.8 |                 36.4% |
|      Monroe |                    1.1 |                            14.8 |                 36.4% |
|     Clayton |                    2.0 |                            11.4 |                 31.2% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Lee |                    2.9 |                             8.5 |               \-70.0% |
|   Jasper |                    3.1 |                             8.5 |               \-67.4% |
|   Shelby |                    1.1 |                            10.0 |               \-64.3% |
|  Wapello |                    1.7 |                             4.9 |               \-52.5% |
| Humboldt |                    0.4 |                             4.5 |               \-52.4% |
|    Mills |                    1.1 |                             7.6 |               \-50.0% |
| Mitchell |                    0.7 |                             6.7 |               \-45.5% |
|   Dallas |                   13.7 |                            14.7 |               \-45.2% |
| Cherokee |                    1.3 |                            11.4 |               \-44.8% |
|  Webster |                    2.0 |                             5.6 |               \-41.7% |
