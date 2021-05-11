Compiled at 2021-05-11 20:19:36 UTC

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

## Tables as of 2021-05-11

As of 2021-05-11, IPDH is reporting 299 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   52.9 |                            10.8 |               \-14.9% |
|          Linn |                   19.4 |                             8.6 |                \-8.3% |
|         Scott |                   34.9 |                            20.2 |               \-14.6% |
|       Johnson |                   11.6 |                             7.7 |               \-30.7% |
|    Black Hawk |                    7.4 |                             5.7 |               \-26.2% |
|      Woodbury |                    6.1 |                             6.0 |               \-24.2% |
|       Dubuque |                    7.1 |                             7.3 |               \-10.9% |
|         Story |                    8.7 |                             9.0 |               \-38.2% |
|        Dallas |                    9.3 |                             9.9 |               \-15.3% |
| Pottawattamie |                   10.9 |                            11.6 |               \-29.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Calhoun |                    3.6 |                            36.9 |                 60.0% |
|  Ringgold |                    1.6 |                            32.1 |                 28.6% |
|  Franklin |                    3.1 |                            31.2 |                 16.0% |
|     Davis |                    2.6 |                            28.6 |                108.3% |
|    Jasper |                    8.9 |                            23.8 |                155.6% |
|   Audubon |                    1.3 |                            23.4 |                 77.8% |
| Muscatine |                    8.7 |                            20.4 |                 28.3% |
|     Scott |                   34.9 |                            20.2 |               \-14.6% |
|     Worth |                    1.4 |                            19.4 |               \-15.0% |
|    Wright |                    2.4 |                            19.3 |                 33.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    8.9 |                            23.8 |                155.6% |
|      Davis |                    2.6 |                            28.6 |                108.3% |
|    Audubon |                    1.3 |                            23.4 |                 77.8% |
|    Osceola |                    1.1 |                            19.2 |                 66.6% |
|    Calhoun |                    3.6 |                            36.9 |                 60.0% |
|   Crawford |                    2.9 |                            17.0 |                 58.8% |
|    Kossuth |                    1.0 |                             6.8 |                 40.0% |
|   Hamilton |                    0.6 |                             3.9 |                 37.4% |
|   Mitchell |                    0.6 |                             5.4 |                 37.4% |
| Washington |                    2.7 |                            12.4 |                 36.8% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                    1.1 |                             9.3 |               \-66.7% |
|     Monona |                  \-0.1 |                           \-1.7 |               \-62.5% |
|       Lyon |                    0.1 |                             1.2 |               \-57.9% |
|  Dickinson |                    0.7 |                             4.1 |               \-55.6% |
|     Hardin |                    0.7 |                             4.2 |               \-52.0% |
|   Harrison |                    0.4 |                             3.1 |               \-50.0% |
| Pocahontas |                  \-0.1 |                           \-2.2 |               \-50.0% |
|      Cedar |                    1.0 |                             5.4 |               \-48.1% |
|       Cass |                    0.4 |                             3.3 |               \-47.3% |
|     Benton |                    1.4 |                             5.6 |               \-45.2% |
