Compiled at 2021-03-16 00:03:50 UTC

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

## Tables as of 2021-03-15

As of 2021-03-15, IPDH is reporting 190 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-15 |                  462.9 |                            14.7 |                \-4.2% |
| 2021-03-14 |                  505.0 |                            16.0 |                  8.9% |
| 2021-03-13 |                  464.7 |                            14.7 |               \-14.4% |
| 2021-03-12 |                  520.7 |                            16.5 |                  3.9% |
| 2021-03-11 |                  546.7 |                            17.3 |                  9.6% |
| 2021-03-10 |                  577.4 |                            18.3 |                 12.8% |
| 2021-03-09 |                  528.3 |                            16.7 |                \-1.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   98.3 |                            20.1 |                  4.7% |
|          Linn |                   13.1 |                             5.8 |               \-24.4% |
|         Scott |                   22.9 |                            13.2 |                  2.5% |
|       Johnson |                    9.4 |                             6.2 |               \-39.7% |
|    Black Hawk |                   15.9 |                            12.1 |                 12.4% |
|      Woodbury |                   29.6 |                            28.7 |                 41.7% |
|       Dubuque |                    8.0 |                             8.2 |               \-31.5% |
|         Story |                   14.3 |                            14.7 |               \-22.5% |
|        Dallas |                   18.9 |                            20.2 |                  6.1% |
| Pottawattamie |                   12.1 |                            13.0 |               \-19.3% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Ida |                    4.0 |                            58.3 |                 59.1% |
|      Clay |                    6.9 |                            42.8 |                139.1% |
| Dickinson |                    7.3 |                            42.2 |                 61.1% |
|  Cherokee |                    4.7 |                            42.0 |                 37.9% |
|      Page |                    5.1 |                            34.0 |                104.8% |
|     Wayne |                    2.1 |                            33.3 |               \-33.3% |
|   Madison |                    5.4 |                            33.2 |                 55.2% |
|  Woodbury |                   29.6 |                            28.7 |                 41.7% |
|   Wapello |                    9.4 |                            27.0 |                \-2.7% |
| Winnebago |                    2.7 |                            26.2 |                 23.8% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Carroll |                    5.0 |                            24.8 |                162.5% |
|      Clay |                    6.9 |                            42.8 |                139.1% |
|      Lyon |                    2.6 |                            21.9 |                108.3% |
|      Page |                    5.1 |                            34.0 |                104.8% |
|   Kossuth |                    3.9 |                            26.0 |                 79.0% |
|     Mills |                    2.6 |                            17.0 |                 66.6% |
| Dickinson |                    7.3 |                            42.2 |                 61.1% |
|       Ida |                    4.0 |                            58.3 |                 59.1% |
|   Madison |                    5.4 |                            33.2 |                 55.2% |
|    Monona |                    1.4 |                            16.6 |                 54.6% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Fayette |                    0.9 |                             4.4 |               \-60.6% |
|   Fremont |                  \-0.1 |                           \-2.1 |               \-57.2% |
| Chickasaw |                    0.4 |                             3.6 |               \-52.4% |
|      Tama |                    1.0 |                             5.9 |               \-48.1% |
|       Lee |                    0.4 |                             1.3 |               \-47.3% |
| Allamakee |                    2.7 |                            19.8 |               \-46.9% |
|      Cass |                    2.0 |                            15.6 |               \-46.1% |
|    Butler |                    0.7 |                             4.9 |               \-45.5% |
|    Keokuk |                    0.4 |                             4.2 |               \-44.4% |
|   O’Brien |                    2.9 |                            20.8 |               \-43.8% |
