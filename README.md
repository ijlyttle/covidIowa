Compiled at 2021-08-17 23:53:33 UTC

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

## Tables as of 2021-08-12

As of 2021-08-12, IPDH is reporting 4872 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  247.6 |                            50.5 |              1 160.9% |
|          Linn |                  108.4 |                            47.8 |              1 640.8% |
|         Scott |                   78.6 |                            45.4 |                844.0% |
|       Johnson |                   51.6 |                            34.1 |                922.2% |
|    Black Hawk |                  114.6 |                            87.3 |                499.2% |
|      Woodbury |                   56.4 |                            54.7 |                673.0% |
|       Dubuque |                   26.1 |                            26.9 |                900.1% |
|         Story |                   47.0 |                            48.4 |                983.8% |
|        Dallas |                   48.0 |                            51.4 |                939.5% |
| Pottawattamie |                   59.7 |                            64.1 |              1 048.6% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   61.4 |                           182.5 |              1 580.9% |
|    Webster |                   49.3 |                           137.3 |                334.6% |
|        Ida |                    8.3 |                           120.8 |                828.6% |
|   Crawford |                   17.9 |                           106.2 |                779.9% |
| Des Moines |                   41.0 |                           105.2 |                653.9% |
|   Franklin |                    9.3 |                            92.2 |                213.0% |
|   Hamilton |                   13.6 |                            91.9 |                343.4% |
| Black Hawk |                  114.6 |                            87.3 |                499.2% |
|    Kossuth |                   12.9 |                            86.8 |                546.6% |
|   Humboldt |                    8.3 |                            86.7 |                242.2% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Linn |                  108.4 |                            47.8 |              1 640.8% |
|           Lee |                   61.4 |                           182.5 |              1 580.9% |
|          Polk |                  247.6 |                            50.5 |              1 160.9% |
| Pottawattamie |                   59.7 |                            64.1 |              1 048.6% |
|       Fayette |                   10.0 |                            50.9 |              1 000.0% |
|         Story |                   47.0 |                            48.4 |                983.8% |
|        Dallas |                   48.0 |                            51.4 |                939.5% |
|       Johnson |                   51.6 |                            34.1 |                922.2% |
|       Dubuque |                   26.1 |                            26.9 |                900.1% |
|         Henry |                   13.1 |                            65.9 |                889.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Montgomery |                    1.7 |                            17.3 |                 11.7% |
|    Calhoun |                    6.0 |                            62.1 |                 69.0% |
|      Adair |                    2.7 |                            37.9 |                 73.3% |
|   Ringgold |                    1.3 |                            26.3 |                 77.8% |
|   Mitchell |                    1.9 |                            17.5 |                 81.9% |
|    Decatur |                    3.9 |                            49.0 |                 88.9% |
|     Monona |                    2.9 |                            33.2 |                 92.9% |
|     Taylor |                    1.0 |                            16.3 |                100.0% |
|      Adams |                    2.3 |                            63.5 |                109.2% |
| Pocahontas |                    1.7 |                            25.9 |                111.0% |
