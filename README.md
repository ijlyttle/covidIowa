Compiled at 2021-05-08 23:58:36 UTC

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

## Tables as of 2021-05-08

As of 2021-05-08, IPDH is reporting 300 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   61.9 |                            12.6 |                  0.2% |
|          Linn |                   22.7 |                            10.0 |                 15.3% |
|         Scott |                   38.9 |                            22.5 |                  4.9% |
|       Johnson |                   12.0 |                             7.9 |               \-34.5% |
|    Black Hawk |                    8.1 |                             6.2 |               \-19.0% |
|      Woodbury |                    6.7 |                             6.5 |               \-18.2% |
|       Dubuque |                    8.0 |                             8.2 |                \-8.7% |
|         Story |                   11.4 |                            11.8 |               \-17.9% |
|        Dallas |                   10.9 |                            11.6 |                  9.2% |
| Pottawattamie |                   12.7 |                            13.6 |               \-13.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Madison |                    5.7 |                            35.0 |                135.0% |
|   Calhoun |                    3.3 |                            34.0 |                 36.4% |
|  Ringgold |                    1.6 |                            32.1 |                 20.0% |
|  Franklin |                    3.1 |                            31.2 |                 11.6% |
|     Davis |                    2.3 |                            25.4 |                 77.0% |
|     Emmet |                    2.1 |                            23.3 |                  4.8% |
|     Scott |                   38.9 |                            22.5 |                  4.9% |
| Muscatine |                    9.1 |                            21.4 |                 51.1% |
|    Jasper |                    7.6 |                            20.4 |                100.0% |
|    Wright |                    2.4 |                            19.3 |                 26.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Madison |                    5.7 |                            35.0 |                135.0% |
|     Jasper |                    7.6 |                            20.4 |                100.0% |
|      Sioux |                    4.4 |                            12.7 |                 90.0% |
|      Davis |                    2.3 |                            25.4 |                 77.0% |
|    Audubon |                    1.0 |                            18.2 |                 75.0% |
|    Wapello |                    2.9 |                             8.2 |                 68.7% |
| Washington |                    3.0 |                            13.7 |                 64.7% |
|   Crawford |                    3.0 |                            17.8 |                 64.7% |
|        Lee |                    4.1 |                            12.3 |                 63.6% |
|     Butler |                    1.7 |                            11.9 |                 58.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Pocahontas |                    0.0 |                             0.0 |               \-53.3% |
|   Dickinson |                    1.0 |                             5.8 |               \-51.7% |
|      Hardin |                    0.9 |                             5.1 |               \-50.0% |
|       Union |                    2.0 |                            16.3 |               \-47.5% |
| Buena Vista |                    0.4 |                             2.2 |               \-41.2% |
|       Adair |                    0.4 |                             6.0 |               \-41.2% |
| Cerro Gordo |                    5.0 |                            11.8 |               \-40.0% |
|      Howard |                    0.3 |                             3.1 |               \-40.0% |
|    Delaware |                    1.4 |                             8.4 |               \-39.3% |
|       Adams |                    0.1 |                             4.0 |               \-38.4% |
