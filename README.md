Compiled at 2021-05-13 20:18:39 UTC

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

## Tables as of 2021-05-13

As of 2021-05-13, IPDH is reporting 305 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   44.9 |                             9.2 |               \-30.1% |
|          Linn |                   17.7 |                             7.8 |               \-12.1% |
|         Scott |                   33.0 |                            19.1 |               \-14.4% |
|       Johnson |                    9.4 |                             6.2 |               \-25.5% |
|    Black Hawk |                    6.9 |                             5.2 |               \-24.7% |
|      Woodbury |                    4.7 |                             4.6 |               \-42.0% |
|       Dubuque |                    5.9 |                             6.0 |               \-15.8% |
|         Story |                    9.7 |                            10.0 |               \-16.7% |
|        Dallas |                    9.9 |                            10.5 |                  2.7% |
| Pottawattamie |                    9.9 |                            10.6 |               \-25.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Franklin |                    4.1 |                            41.1 |                 44.0% |
|   Calhoun |                    3.0 |                            31.0 |                 21.7% |
|     Worth |                    1.7 |                            23.2 |                 72.8% |
| Winnebago |                    2.3 |                            22.1 |                  9.5% |
|    Jasper |                    7.4 |                            20.0 |                136.0% |
| Muscatine |                    8.4 |                            19.8 |                \-1.5% |
|     Scott |                   33.0 |                            19.1 |               \-14.4% |
|   Hancock |                    1.9 |                            17.5 |                 11.1% |
|  Crawford |                    2.9 |                            17.0 |                 58.8% |
|   Osceola |                    1.0 |                            16.8 |                 27.3% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Jasper |                    7.4 |                            20.0 |                136.0% |
|  Mitchell |                    1.0 |                             9.4 |                 75.0% |
|     Worth |                    1.7 |                            23.2 |                 72.8% |
|    Howard |                    0.7 |                             7.8 |                 71.4% |
|  Crawford |                    2.9 |                            17.0 |                 58.8% |
|  Franklin |                    4.1 |                            41.1 |                 44.0% |
| Allamakee |                    1.6 |                            11.5 |                 38.4% |
|    Keokuk |                    0.6 |                             5.6 |                 37.4% |
|    Grundy |                    0.7 |                             5.8 |                 33.3% |
|      Cass |                    1.4 |                            11.1 |                 30.8% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    0.7 |                             5.8 |               \-72.1% |
|  Ringgold |                    0.1 |                             2.9 |               \-65.2% |
|     Henry |                    0.7 |                             3.6 |               \-53.9% |
|    Monona |                  \-0.1 |                           \-1.7 |               \-50.0% |
|     Emmet |                    0.7 |                             7.8 |               \-47.8% |
|   Decatur |                    0.3 |                             3.6 |               \-47.1% |
|   Mahaska |                    1.3 |                             5.8 |               \-46.7% |
| Poweshiek |                    0.1 |                             0.8 |               \-46.7% |
|  Harrison |                    0.4 |                             3.1 |               \-44.4% |
|    Clarke |                    0.4 |                             4.6 |               \-44.4% |
