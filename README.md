Compiled at 2021-04-28 20:19:56 UTC

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

## Tables as of 2021-04-28

As of 2021-04-28, IPDH is reporting 503 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |
| 2021-04-24 |                  488.3 |                            15.5 |                 22.1% |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   68.9 |                            14.0 |               \-14.1% |
|          Linn |                   23.7 |                            10.5 |               \-10.4% |
|         Scott |                   33.1 |                            19.2 |               \-38.7% |
|       Johnson |                   19.4 |                            12.9 |               \-35.3% |
|    Black Hawk |                   10.3 |                             7.8 |               \-34.7% |
|      Woodbury |                   10.3 |                            10.0 |               \-33.0% |
|       Dubuque |                    9.1 |                             9.4 |               \-36.0% |
|         Story |                   13.4 |                            13.8 |                 12.2% |
|        Dallas |                   11.1 |                            11.9 |                \-6.6% |
| Pottawattamie |                   18.4 |                            19.8 |                \-9.3% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Emmet |                    2.9 |                            31.0 |                  8.0% |
|       Worth |                    2.3 |                            31.0 |                 27.8% |
|   Winnebago |                    3.1 |                            30.4 |                 31.8% |
|       Floyd |                    3.6 |                            22.8 |                 60.0% |
|    Franklin |                    2.3 |                            22.7 |                 77.0% |
|  Pocahontas |                    1.4 |                            21.6 |                 21.5% |
| Cerro Gordo |                    9.1 |                            21.5 |                 26.8% |
|     Carroll |                    4.3 |                            21.3 |                 76.2% |
|      Warren |                   10.6 |                            20.5 |                \-4.7% |
|    Delaware |                    3.4 |                            20.2 |                  0.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Union |                    1.0 |                             8.2 |                   Inf |
|    Marshall |                    3.1 |                             8.0 |                107.1% |
|   Appanoose |                    1.1 |                             9.2 |                 87.5% |
|    Franklin |                    2.3 |                            22.7 |                 77.0% |
|     Carroll |                    4.3 |                            21.3 |                 76.2% |
|       Davis |                    0.7 |                             7.9 |                 71.4% |
|        Tama |                    1.9 |                            11.0 |                 66.7% |
| Buena Vista |                    2.3 |                            11.7 |                 64.3% |
|      Howard |                    1.6 |                            17.2 |                 63.7% |
|      Jasper |                    3.4 |                             9.2 |                 63.2% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Plymouth |                    0.6 |                             2.3 |               \-69.5% |
|       Ida |                  \-0.3 |                           \-4.2 |               \-68.8% |
|   Osceola |                    0.6 |                             9.6 |               \-64.5% |
|    Shelby |                    0.7 |                             6.2 |               \-60.0% |
|     Boone |                    1.1 |                             4.4 |               \-54.5% |
|  Crawford |                    0.3 |                             1.7 |               \-52.6% |
|    Louisa |                    0.3 |                             2.6 |               \-47.1% |
| Palo Alto |                    0.7 |                             8.0 |               \-45.5% |
|   Mahaska |                    1.0 |                             4.5 |               \-44.0% |
|  Humboldt |                    0.0 |                             0.0 |               \-41.7% |
