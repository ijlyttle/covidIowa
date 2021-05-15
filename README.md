Compiled at 2021-05-15 00:01:31 UTC

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

## Tables as of 2021-05-14

As of 2021-05-14, IPDH is reporting 253 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   43.7 |                             8.9 |               \-31.2% |
|          Linn |                   16.6 |                             7.3 |               \-20.6% |
|         Scott |                   28.3 |                            16.4 |               \-26.0% |
|       Johnson |                    8.6 |                             5.7 |               \-27.2% |
|    Black Hawk |                    7.1 |                             5.4 |               \-19.7% |
|      Woodbury |                    4.9 |                             4.7 |               \-34.9% |
|       Dubuque |                    5.4 |                             5.6 |               \-27.4% |
|         Story |                    7.6 |                             7.8 |               \-33.3% |
|        Dallas |                    7.9 |                             8.4 |               \-25.3% |
| Pottawattamie |                    9.4 |                            10.1 |               \-33.6% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Franklin |                    4.4 |                            44.0 |                 31.0% |
|    Calhoun |                    2.3 |                            23.6 |               \-14.8% |
|    Hancock |                    2.1 |                            20.2 |                 57.1% |
|  Muscatine |                    8.4 |                            19.8 |                  0.0% |
|    Osceola |                    1.1 |                            19.2 |                 50.0% |
|     Jasper |                    7.0 |                            18.8 |                 86.7% |
|      Worth |                    1.3 |                            17.4 |                 23.1% |
| Des Moines |                    6.6 |                            16.9 |                 20.4% |
|  Winnebago |                    1.7 |                            16.6 |                \-9.5% |
|      Scott |                   28.3 |                            16.4 |               \-26.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                    7.0 |                            18.8 |                 86.7% |
|         Ida |                    0.4 |                             6.3 |                 66.7% |
|     Hancock |                    2.1 |                            20.2 |                 57.1% |
|    Cherokee |                    0.7 |                             6.4 |                 50.0% |
|     Osceola |                    1.1 |                            19.2 |                 50.0% |
| Buena Vista |                    0.9 |                             4.4 |                 44.4% |
|    Mitchell |                    0.9 |                             8.1 |                 44.4% |
|    Hamilton |                    1.0 |                             6.8 |                 40.0% |
|      Keokuk |                    0.7 |                             7.0 |                 33.3% |
|    Delaware |                    2.0 |                            11.8 |                 31.2% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Washington |                    0.3 |                             1.3 |               \-70.0% |
|      Union |                    0.4 |                             3.5 |               \-66.7% |
|      Emmet |                    0.4 |                             4.7 |               \-56.5% |
|   Ringgold |                    0.4 |                             8.8 |               \-54.5% |
|  Poweshiek |                    0.0 |                             0.0 |               \-53.3% |
|    Kossuth |                    0.1 |                             1.0 |               \-50.0% |
|    Carroll |                    0.9 |                             4.2 |               \-48.0% |
|    Madison |                    2.3 |                            14.0 |               \-47.7% |
|    Clayton |                    0.3 |                             1.6 |               \-47.1% |
|    Decatur |                    0.3 |                             3.6 |               \-47.1% |
