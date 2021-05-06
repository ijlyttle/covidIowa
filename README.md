Compiled at 2021-05-06 20:17:16 UTC

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

## Tables as of 2021-05-06

As of 2021-05-06, IPDH is reporting 711 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   64.6 |                            13.2 |                \-4.6% |
|          Linn |                   20.3 |                             8.9 |               \-13.9% |
|         Scott |                   38.7 |                            22.4 |                 12.5% |
|       Johnson |                   13.0 |                             8.6 |               \-27.9% |
|    Black Hawk |                    9.4 |                             7.2 |                \-7.6% |
|      Woodbury |                    8.9 |                             8.6 |                \-5.5% |
|       Dubuque |                    7.1 |                             7.3 |               \-16.2% |
|         Story |                   11.9 |                            12.2 |                \-9.1% |
|        Dallas |                    9.6 |                            10.2 |               \-21.3% |
| Pottawattamie |                   13.6 |                            14.6 |               \-17.1% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Ringgold |                    2.3 |                            46.7 |                130.0% |
|     Union |                    5.1 |                            42.0 |                168.7% |
|   Madison |                    5.1 |                            31.5 |                 95.5% |
|  Franklin |                    2.6 |                            25.5 |                  0.0% |
|     Emmet |                    2.3 |                            24.8 |                \-8.0% |
|   Calhoun |                    2.3 |                            23.6 |                 15.0% |
|   Audubon |                    1.3 |                            23.4 |                 60.0% |
|     Scott |                   38.7 |                            22.4 |                 12.5% |
|     Davis |                    1.9 |                            20.6 |                 53.9% |
| Muscatine |                    8.6 |                            20.1 |                 24.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.1 |                            42.0 |                168.7% |
|  Ringgold |                    2.3 |                            46.7 |                130.0% |
|    Butler |                    1.9 |                            12.9 |                122.2% |
|   Mahaska |                    3.3 |                            14.9 |                100.0% |
|    Clarke |                    1.6 |                            16.7 |                 99.9% |
|   Madison |                    5.1 |                            31.5 |                 95.5% |
| Chickasaw |                    1.1 |                             9.6 |                 87.5% |
|   Wapello |                    3.0 |                             8.6 |                 86.7% |
|  Plymouth |                    1.4 |                             5.7 |                 70.0% |
|       Ida |                    0.4 |                             6.3 |                 66.7% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Howard |                    0.0 |                             0.0 |               \-61.1% |
|       Worth |                    0.6 |                             7.7 |               \-54.2% |
|       Adair |                    0.3 |                             4.0 |               \-52.6% |
|       Floyd |                    1.1 |                             7.3 |               \-51.6% |
|  Pocahontas |                    0.3 |                             4.3 |               \-47.1% |
| Buena Vista |                    0.4 |                             2.2 |               \-44.4% |
|        Cass |                    0.9 |                             6.7 |               \-43.5% |
|        Clay |                    0.7 |                             4.5 |               \-42.9% |
|    Delaware |                    1.7 |                            10.1 |               \-38.7% |
| Cerro Gordo |                    5.4 |                            12.8 |               \-38.4% |
