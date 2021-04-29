Compiled at 2021-04-29 17:10:16 UTC

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

## Tables as of 2021-04-29

As of 2021-04-29, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-29 |                  302.6 |                             9.6 |               \-32.3% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   57.7 |                            11.8 |               \-27.9% |
|          Linn |                   19.6 |                             8.6 |               \-21.7% |
|         Scott |                   25.9 |                            15.0 |               \-48.8% |
|       Johnson |                   14.9 |                             9.8 |               \-49.8% |
|    Black Hawk |                    8.7 |                             6.6 |               \-39.8% |
|      Woodbury |                    7.9 |                             7.6 |               \-42.1% |
|       Dubuque |                    7.1 |                             7.3 |               \-47.7% |
|         Story |                   11.1 |                            11.5 |                \-7.6% |
|        Dallas |                    9.6 |                            10.2 |               \-12.9% |
| Pottawattamie |                   14.1 |                            15.2 |               \-26.4% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Worth |                    2.3 |                            31.0 |                 64.3% |
|   Winnebago |                    2.9 |                            27.6 |                 28.6% |
|       Emmet |                    2.1 |                            23.3 |               \-18.5% |
|       Floyd |                    3.1 |                            20.1 |                 52.7% |
|       Adair |                    1.4 |                            20.0 |                 41.7% |
|    Franklin |                    2.0 |                            19.9 |                 40.0% |
| Cerro Gordo |                    8.4 |                            19.9 |                 13.8% |
|    Delaware |                    3.1 |                            18.5 |                \-3.3% |
|       Cedar |                    3.4 |                            18.4 |                 29.2% |
|     Carroll |                    3.3 |                            16.3 |                 30.4% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    0.9 |                             7.0 |                   Inf |
| Appanoose |                    1.1 |                             9.2 |                150.1% |
|  Marshall |                    3.0 |                             7.6 |                100.0% |
|     Davis |                    0.7 |                             7.9 |                 71.4% |
|     Worth |                    2.3 |                            31.0 |                 64.3% |
|    Howard |                    1.4 |                            15.6 |                 54.6% |
|     Floyd |                    3.1 |                            20.1 |                 52.7% |
|    Jasper |                    2.9 |                             7.7 |                 42.1% |
|     Adair |                    1.4 |                            20.0 |                 41.7% |
|  Franklin |                    2.0 |                            19.9 |                 40.0% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Osceola |                    0.3 |                             4.8 |               \-70.0% |
| Plymouth |                    0.4 |                             1.7 |               \-65.5% |
|  Mahaska |                    0.4 |                             1.9 |               \-65.5% |
|   Shelby |                    0.4 |                             3.7 |               \-64.3% |
|      Ida |                  \-0.3 |                           \-4.2 |               \-64.3% |
|     Clay |                    1.6 |                             9.8 |               \-55.0% |
|      Sac |                    0.9 |                             8.8 |               \-51.9% |
|   Hardin |                    1.4 |                             8.5 |               \-51.4% |
|    Boone |                    1.1 |                             4.4 |               \-50.0% |
|   Louisa |                    0.1 |                             1.3 |               \-50.0% |
