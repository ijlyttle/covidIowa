Compiled at 2021-04-24 00:03:20 UTC

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

## Tables as of 2021-04-23

As of 2021-04-23, IPDH is reporting 431 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-23 |                  426.0 |                            13.5 |               \-12.7% |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   79.1 |                            16.1 |                \-6.0% |
|          Linn |                   24.6 |                            10.8 |                \-7.3% |
|         Scott |                   41.6 |                            24.0 |               \-32.7% |
|       Johnson |                   26.9 |                            17.8 |               \-14.5% |
|    Black Hawk |                   13.9 |                            10.6 |                \-7.1% |
|      Woodbury |                   15.0 |                            14.5 |               \-30.0% |
|       Dubuque |                   13.7 |                            14.1 |               \-33.1% |
|         Story |                   11.9 |                            12.2 |                  3.4% |
|        Dallas |                   12.4 |                            13.3 |                \-4.1% |
| Pottawattamie |                   19.4 |                            20.8 |               \-13.9% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    3.3 |                            55.2 |                 15.4% |
|     Emmet |                    3.0 |                            32.6 |                 27.3% |
| Dickinson |                    4.9 |                            28.1 |                \-8.9% |
|       Sac |                    2.7 |                            27.9 |                 13.0% |
|     Scott |                   41.6 |                            24.0 |               \-32.7% |
| Winnebago |                    2.4 |                            23.5 |                 71.4% |
|    Hardin |                    3.9 |                            22.9 |                 30.8% |
|      Clay |                    3.6 |                            22.3 |                \-8.6% |
|  Delaware |                    3.7 |                            21.8 |                  3.1% |
|    Warren |                   11.1 |                            21.7 |                \-6.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Lucas |                    1.6 |                            18.3 |                124.9% |
|  Jefferson |                    1.1 |                             6.2 |                114.3% |
|   Franklin |                    1.3 |                            12.8 |                 77.8% |
|      Henry |                    2.4 |                            12.2 |                 71.4% |
|  Winnebago |                    2.4 |                            23.5 |                 71.4% |
|     Keokuk |                    1.0 |                             9.8 |                 55.5% |
| Pocahontas |                    1.4 |                            21.6 |                 54.6% |
|       Cass |                    1.9 |                            14.5 |                 53.9% |
|  Allamakee |                    0.7 |                             5.2 |                 50.0% |
|     Monona |                    1.6 |                            18.2 |                 50.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
|       Page |                    0.7 |                             4.7 |               \-57.2% |
| Washington |                    0.9 |                             3.9 |               \-53.6% |
|    Clayton |                    0.7 |                             4.1 |               \-50.0% |
|   Buchanan |                    1.0 |                             4.7 |               \-44.0% |
| Winneshiek |                    1.4 |                             7.1 |               \-43.3% |
|    Wapello |                    0.9 |                             2.5 |               \-40.9% |
|     Butler |                    0.3 |                             2.0 |               \-40.0% |
|        Ida |                    0.7 |                            10.4 |               \-40.0% |
|    Fremont |                    0.6 |                             8.2 |               \-38.9% |
