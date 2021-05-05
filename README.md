Compiled at 2021-05-05 23:59:56 UTC

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

## Tables as of 2021-05-05

As of 2021-05-05, IPDH is reporting 138 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   54.4 |                            11.1 |               \-20.7% |
|          Linn |                   17.7 |                             7.8 |               \-24.3% |
|         Scott |                   36.1 |                            20.9 |                  8.8% |
|       Johnson |                   13.1 |                             8.7 |               \-30.8% |
|    Black Hawk |                    8.0 |                             6.1 |               \-20.3% |
|      Woodbury |                    8.3 |                             8.0 |               \-17.7% |
|       Dubuque |                    6.7 |                             6.9 |               \-23.9% |
|         Story |                   11.4 |                            11.8 |               \-13.9% |
|        Dallas |                    9.6 |                            10.2 |               \-12.9% |
| Pottawattamie |                   13.0 |                            13.9 |               \-27.9% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    4.9 |                            39.7 |                192.9% |
|   Madison |                    4.4 |                            27.1 |                 52.0% |
|  Franklin |                    2.1 |                            21.3 |                \-4.4% |
|     Scott |                   36.1 |                            20.9 |                  8.8% |
| Winnebago |                    2.1 |                            20.7 |               \-24.1% |
|     Emmet |                    1.7 |                            18.6 |               \-29.6% |
| Muscatine |                    7.9 |                            18.4 |                 29.2% |
|   Decatur |                    1.4 |                            18.2 |                 54.6% |
|   Calhoun |                    1.7 |                            17.7 |                 26.6% |
|  Ringgold |                    0.9 |                            17.5 |                 44.4% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    4.9 |                            39.7 |                192.9% |
|   Mahaska |                    3.4 |                            15.5 |                121.4% |
|  Crawford |                    1.7 |                            10.2 |                111.0% |
|       Ida |                    0.3 |                             4.2 |                 80.1% |
|    Butler |                    1.3 |                             8.9 |                 77.8% |
|     Boone |                    2.4 |                             9.3 |                 60.0% |
|   Decatur |                    1.4 |                            18.2 |                 54.6% |
|   Madison |                    4.4 |                            27.1 |                 52.0% |
|   Wapello |                    2.1 |                             6.1 |                 46.7% |
| Chickasaw |                    0.9 |                             7.2 |                 44.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    0.3 |                             1.5 |               \-60.9% |
|      Howard |                    0.1 |                             1.6 |               \-55.5% |
|       Floyd |                    1.1 |                             7.3 |               \-53.1% |
|       Worth |                    0.6 |                             7.7 |               \-52.2% |
|   Jefferson |                    0.1 |                             0.8 |               \-50.0% |
|       Adair |                    0.3 |                             4.0 |               \-47.1% |
|     Kossuth |                    0.1 |                             1.0 |               \-46.7% |
|     Carroll |                    1.9 |                             9.2 |               \-46.0% |
| Cerro Gordo |                    4.7 |                            11.1 |               \-43.7% |
|     O’Brien |                    0.6 |                             4.2 |               \-42.1% |
