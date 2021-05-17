Compiled at 2021-05-17 20:21:49 UTC

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

## Tables as of 2021-05-17

As of 2021-05-17, IPDH is reporting 86 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   39.3 |                             8.0 |               \-28.2% |
|          Linn |                   19.1 |                             8.4 |                \-1.4% |
|         Scott |                   24.1 |                            14.0 |               \-30.7% |
|       Johnson |                    7.9 |                             5.2 |               \-21.5% |
|    Black Hawk |                    7.1 |                             5.4 |                  7.6% |
|      Woodbury |                    6.3 |                             6.1 |                  8.5% |
|       Dubuque |                    5.0 |                             5.1 |               \-30.0% |
|         Story |                    6.7 |                             6.9 |               \-30.8% |
|        Dallas |                    5.9 |                             6.3 |               \-39.2% |
| Pottawattamie |                    8.6 |                             9.2 |               \-24.7% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Franklin |                    3.6 |                            35.5 |                  0.0% |
|    Hancock |                    2.1 |                            20.2 |                 22.2% |
| Des Moines |                    7.6 |                            19.4 |                 30.4% |
|    Calhoun |                    1.9 |                            19.2 |               \-31.0% |
|  Muscatine |                    8.0 |                            18.8 |                  8.6% |
|    Osceola |                    0.9 |                            14.4 |                  0.0% |
|      Davis |                    1.3 |                            14.3 |               \-36.0% |
|      Scott |                   24.1 |                            14.0 |               \-30.7% |
|  Winnebago |                    1.4 |                            13.8 |               \-10.5% |
|      Worth |                    1.0 |                            13.5 |               \-17.7% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Buchanan |                    1.4 |                             6.7 |                 88.9% |
|    Cherokee |                    0.7 |                             6.4 |                 50.0% |
|    Hamilton |                    1.3 |                             8.7 |                 45.5% |
|     Jackson |                    1.4 |                             7.4 |                 30.8% |
|  Des Moines |                    7.6 |                            19.4 |                 30.4% |
| Buena Vista |                    0.9 |                             4.4 |                 30.0% |
|        Iowa |                    1.0 |                             6.2 |                 27.3% |
|    Humboldt |                    0.4 |                             4.5 |                 25.0% |
|     Hancock |                    2.1 |                            20.2 |                 22.2% |
|       Floyd |                    1.6 |                            10.0 |                 20.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    2.1 |                             5.8 |               \-65.1% |
|   Crawford |                    0.6 |                             3.4 |               \-59.3% |
|      Emmet |                    0.3 |                             3.1 |               \-57.1% |
| Washington |                    0.9 |                             3.9 |               \-53.6% |
|       Page |                    0.1 |                             0.9 |               \-50.0% |
|      Sioux |                    1.6 |                             4.5 |               \-48.6% |
|    Decatur |                    0.3 |                             3.6 |               \-47.1% |
| Montgomery |                    0.1 |                             1.4 |               \-46.7% |
|    Madison |                    1.6 |                             9.6 |               \-45.5% |
|   Ringgold |                    0.4 |                             8.8 |               \-44.4% |
