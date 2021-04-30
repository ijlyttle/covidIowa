Compiled at 2021-04-30 00:00:12 UTC

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

As of 2021-04-29, IPDH is reporting 475 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   67.7 |                            13.8 |               \-15.6% |
|          Linn |                   23.7 |                            10.5 |                \-6.0% |
|         Scott |                   34.3 |                            19.8 |               \-32.7% |
|       Johnson |                   18.4 |                            12.2 |               \-38.5% |
|    Black Hawk |                   10.3 |                             7.8 |               \-30.1% |
|      Woodbury |                    9.4 |                             9.1 |               \-31.8% |
|       Dubuque |                    8.7 |                             9.0 |               \-37.6% |
|         Story |                   13.1 |                            13.5 |                  7.6% |
|        Dallas |                   12.4 |                            13.3 |                 10.6% |
| Pottawattamie |                   16.6 |                            17.8 |               \-14.6% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Worth |                    2.4 |                            32.9 |                 71.4% |
|   Winnebago |                    3.3 |                            31.7 |                 42.9% |
|       Emmet |                    2.6 |                            27.9 |                \-7.4% |
|    Franklin |                    2.6 |                            25.5 |                 66.6% |
|       Adair |                    1.7 |                            24.0 |                 58.3% |
| Cerro Gordo |                    9.4 |                            22.2 |                 25.9% |
|       Floyd |                    3.4 |                            21.9 |                 63.2% |
|  Pocahontas |                    1.4 |                            21.6 |                  0.0% |
|    Delaware |                    3.4 |                            20.2 |                  3.3% |
|       Scott |                   34.3 |                            19.8 |               \-32.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    1.3 |                            10.5 |                   Inf |
| Appanoose |                    1.3 |                            10.3 |                166.7% |
|  Marshall |                    3.3 |                             8.3 |                114.3% |
|    Jasper |                    4.6 |                            12.3 |                105.3% |
|     Davis |                    0.9 |                             9.5 |                 85.7% |
|   Calhoun |                    1.9 |                            19.2 |                 81.9% |
|     Worth |                    2.4 |                            32.9 |                 71.4% |
|  Franklin |                    2.6 |                            25.5 |                 66.6% |
|    Howard |                    1.6 |                            17.2 |                 63.7% |
|     Floyd |                    3.4 |                            21.9 |                 63.2% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Osceola |                    0.3 |                             4.8 |               \-70.0% |
| Plymouth |                    0.4 |                             1.7 |               \-65.5% |
|   Shelby |                    0.4 |                             3.7 |               \-64.3% |
|      Ida |                  \-0.1 |                           \-2.1 |               \-57.2% |
|   Hardin |                    1.4 |                             8.5 |               \-51.4% |
|  Mahaska |                    1.1 |                             5.2 |               \-48.3% |
|      Sac |                    1.0 |                            10.3 |               \-48.1% |
|     Clay |                    2.0 |                            12.5 |               \-47.5% |
|   Louisa |                    0.3 |                             2.6 |               \-43.7% |
|    Boone |                    1.4 |                             5.4 |               \-43.3% |
