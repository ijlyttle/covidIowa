Compiled at 2021-03-25 20:41:34 UTC

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

## Tables as of 2021-03-25

As of 2021-03-25, IPDH is reporting 633 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |
| 2021-03-19 |                  428.7 |                            13.6 |               \-17.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   97.4 |                            19.9 |                  5.5% |
|          Linn |                   17.9 |                             7.9 |                 21.1% |
|         Scott |                   37.9 |                            21.9 |                 91.5% |
|       Johnson |                   18.0 |                            11.9 |                 64.2% |
|    Black Hawk |                   12.1 |                             9.3 |                  5.7% |
|      Woodbury |                   29.4 |                            28.5 |                  3.4% |
|       Dubuque |                   13.6 |                            13.9 |                 82.1% |
|         Story |                   16.0 |                            16.5 |                 30.8% |
|        Dallas |                   17.1 |                            18.3 |                  9.5% |
| Pottawattamie |                   21.1 |                            22.7 |                 46.2% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   10.1 |                            58.8 |                 11.4% |
|      Clay |                    7.6 |                            47.3 |                 50.0% |
|     Emmet |                    3.6 |                            38.8 |                 14.3% |
|   Osceola |                    2.0 |                            33.6 |                109.9% |
|     Wayne |                    2.0 |                            31.1 |                \-4.5% |
|   Guthrie |                    3.1 |                            29.4 |                107.1% |
|   Kossuth |                    4.3 |                            28.9 |                  2.8% |
|   Fremont |                    2.0 |                            28.7 |                 40.0% |
|  Woodbury |                   29.4 |                            28.5 |                  3.4% |
|   O’Brien |                    3.9 |                            28.0 |                \-2.9% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Jasper |                    8.9 |                            23.8 |                200.0% |
|   Osceola |                    2.0 |                            33.6 |                109.9% |
|   Guthrie |                    3.1 |                            29.4 |                107.1% |
|     Scott |                   37.9 |                            21.9 |                 91.5% |
|    Louisa |                    1.1 |                            10.4 |                 87.5% |
|   Dubuque |                   13.6 |                            13.9 |                 82.1% |
|      Page |                    2.9 |                            18.9 |                 80.0% |
|   Jackson |                    2.6 |                            13.2 |                 78.6% |
| Van Buren |                    0.4 |                             6.1 |                 66.7% |
|   Johnson |                   18.0 |                            11.9 |                 64.2% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Clarke |                    0.1 |                             1.5 |               \-46.7% |
|    Carroll |                    1.9 |                             9.2 |               \-44.4% |
|    Clayton |                    0.6 |                             3.3 |               \-42.1% |
|      Adair |                    0.6 |                             8.0 |               \-38.9% |
| Pocahontas |                    0.4 |                             6.5 |               \-37.5% |
|     Howard |                    0.7 |                             7.8 |               \-36.8% |
|     Bremer |                    1.3 |                             5.1 |               \-36.0% |
|      Cedar |                    1.3 |                             6.9 |               \-33.3% |
|  Winnebago |                    1.1 |                            11.0 |               \-31.8% |
|  Allamakee |                    1.1 |                             8.4 |               \-28.6% |
