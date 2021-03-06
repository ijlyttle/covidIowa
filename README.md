Compiled at 2021-03-06 16:34:15 UTC

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

## Tables as of 2021-03-05

As of 2021-03-05, IPDH is reporting 405 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-05 |                  466.4 |                            14.8 |               \-13.7% |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   86.3 |                            17.6 |               \-23.4% |
|          Linn |                   19.0 |                             8.4 |               \-13.6% |
|         Scott |                   19.4 |                            11.2 |                \-3.4% |
|       Johnson |                   14.4 |                             9.5 |               \-22.3% |
|    Black Hawk |                   12.6 |                             9.6 |               \-15.2% |
|      Woodbury |                   18.1 |                            17.6 |                \-5.0% |
|       Dubuque |                   13.0 |                            13.4 |               \-36.8% |
|         Story |                   18.9 |                            19.4 |                  5.3% |
|        Dallas |                   18.9 |                            20.2 |               \-22.3% |
| Pottawattamie |                   11.1 |                            12.0 |               \-22.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Allamakee |                    5.9 |                            42.8 |                166.7% |
|   O’Brien |                    5.6 |                            40.5 |                 84.0% |
|      Cass |                    4.3 |                            33.4 |                 42.3% |
|     Wayne |                    2.1 |                            33.3 |                 69.3% |
|   Wapello |                   10.9 |                            31.0 |               \-16.2% |
|    Shelby |                    3.3 |                            28.7 |                 66.7% |
|   Audubon |                    1.6 |                            28.6 |                124.9% |
|    Bremer |                    7.1 |                            28.5 |                119.3% |
|     Lucas |                    2.4 |                            28.2 |                 84.7% |
|    Jasper |                   10.4 |                            28.0 |               \-26.6% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Allamakee |                    5.9 |                            42.8 |                166.7% |
| Chickasaw |                    2.0 |                            16.8 |                133.3% |
|   Audubon |                    1.6 |                            28.6 |                124.9% |
|    Bremer |                    7.1 |                            28.5 |                119.3% |
|       Ida |                    1.3 |                            18.7 |                100.0% |
|     Lucas |                    2.4 |                            28.2 |                 84.7% |
|   O’Brien |                    5.6 |                            40.5 |                 84.0% |
|   Fayette |                    3.6 |                            18.2 |                 77.8% |
|  Humboldt |                    2.0 |                            20.9 |                 75.0% |
|     Wayne |                    2.1 |                            33.3 |                 69.3% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    2.0 |                            13.2 |               \-73.4% |
|  Appanoose |                    1.0 |                             8.0 |               \-54.8% |
|        Lee |                    2.6 |                             7.6 |               \-52.8% |
|   Hamilton |                    0.6 |                             3.9 |               \-50.0% |
|      Henry |                    1.0 |                             5.0 |               \-48.1% |
|       Lyon |                    0.4 |                             3.6 |               \-47.3% |
|      Mills |                    0.7 |                             4.7 |               \-45.5% |
|     Louisa |                    0.7 |                             6.5 |               \-42.9% |
| Des Moines |                    4.6 |                            11.7 |               \-42.6% |
|    Jackson |                    1.0 |                             5.1 |               \-41.7% |
