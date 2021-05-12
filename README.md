Compiled at 2021-05-12 20:23:49 UTC

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

## Tables as of 2021-05-12

As of 2021-05-12, IPDH is reporting 374 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   58.0 |                            11.8 |                  6.4% |
|          Linn |                   22.3 |                             9.8 |                 24.4% |
|         Scott |                   38.6 |                            22.3 |                  6.5% |
|       Johnson |                   11.9 |                             7.8 |                \-9.1% |
|    Black Hawk |                    8.3 |                             6.3 |                  3.2% |
|      Woodbury |                    6.4 |                             6.2 |               \-20.0% |
|       Dubuque |                    7.3 |                             7.5 |                  7.4% |
|         Story |                   10.7 |                            11.0 |                \-5.8% |
|        Dallas |                   11.7 |                            12.5 |                 20.3% |
| Pottawattamie |                   11.4 |                            12.3 |               \-11.2% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Franklin |                    4.9 |                            48.2 |                 86.4% |
|   Calhoun |                    4.1 |                            42.9 |                 89.5% |
|  Ringgold |                    1.6 |                            32.1 |                 38.4% |
|     Worth |                    1.9 |                            25.2 |                 81.9% |
|     Davis |                    2.1 |                            23.8 |                 37.5% |
| Winnebago |                    2.4 |                            23.5 |                  9.1% |
|    Jasper |                    8.7 |                            23.4 |                151.9% |
|   Audubon |                    1.3 |                            23.4 |                 60.0% |
|     Scott |                   38.6 |                            22.3 |                  6.5% |
|   Osceola |                    1.3 |                            21.6 |                 77.8% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Jasper |                    8.7 |                            23.4 |                151.9% |
|   Calhoun |                    4.1 |                            42.9 |                 89.5% |
|  Franklin |                    4.9 |                            48.2 |                 86.4% |
|       Lee |                    5.0 |                            14.9 |                 82.6% |
|     Worth |                    1.9 |                            25.2 |                 81.9% |
|   Osceola |                    1.3 |                            21.6 |                 77.8% |
|   Kossuth |                    1.0 |                             6.8 |                 75.0% |
|  Hamilton |                    1.0 |                             6.8 |                 75.0% |
| Allamakee |                    1.6 |                            11.5 |                 63.7% |
|  Mitchell |                    0.9 |                             8.1 |                 62.5% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                    1.4 |                            11.7 |               \-58.5% |
|     Monona |                  \-0.1 |                           \-1.7 |               \-57.2% |
|    Mahaska |                    1.4 |                             6.5 |               \-45.2% |
|       Lyon |                    0.3 |                             2.4 |               \-43.7% |
|    Decatur |                    0.4 |                             5.5 |               \-41.2% |
|  Poweshiek |                    0.3 |                             1.5 |               \-40.0% |
|     Hardin |                    0.7 |                             4.2 |               \-40.0% |
|       Cass |                    0.7 |                             5.6 |               \-33.3% |
| Pocahontas |                    0.1 |                             2.2 |               \-33.3% |
|  Dickinson |                    1.1 |                             6.6 |               \-31.8% |
