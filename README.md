Compiled at 2021-05-11 00:01:25 UTC

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

## Tables as of 2021-05-10

As of 2021-05-10, IPDH is reporting 100 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   55.1 |                            11.2 |               \-11.9% |
|          Linn |                   19.4 |                             8.6 |               \-12.8% |
|         Scott |                   35.3 |                            20.4 |                \-9.9% |
|       Johnson |                   10.3 |                             6.8 |               \-42.8% |
|    Black Hawk |                    6.6 |                             5.0 |               \-37.7% |
|      Woodbury |                    5.7 |                             5.5 |               \-26.6% |
|       Dubuque |                    7.6 |                             7.8 |                \-7.7% |
|         Story |                   10.1 |                            10.4 |               \-29.7% |
|        Dallas |                   10.3 |                            11.0 |                  0.0% |
| Pottawattamie |                   11.7 |                            12.6 |               \-23.3% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
| Franklin |                    3.6 |                            35.5 |                 33.3% |
|  Calhoun |                    3.1 |                            32.5 |                 31.8% |
| Ringgold |                    1.6 |                            32.1 |                 20.0% |
|    Davis |                    2.6 |                            28.6 |                108.3% |
|  Madison |                    3.7 |                            22.7 |                \-2.9% |
|    Emmet |                    2.0 |                            21.7 |                \-4.5% |
|   Jasper |                    8.0 |                            21.5 |                142.3% |
|   Wright |                    2.6 |                            20.5 |                 56.2% |
|    Scott |                   35.3 |                            20.4 |                \-9.9% |
|    Worth |                    1.4 |                            19.4 |               \-15.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    8.0 |                            21.5 |                142.3% |
|      Davis |                    2.6 |                            28.6 |                108.3% |
| Washington |                    3.0 |                            13.7 |                100.0% |
|        Lee |                    4.4 |                            13.2 |                 72.7% |
|      Sioux |                    4.0 |                            11.5 |                 59.1% |
|     Wright |                    2.6 |                            20.5 |                 56.2% |
|    Audubon |                    1.0 |                            18.2 |                 55.5% |
|  Allamakee |                    1.4 |                            10.4 |                 54.6% |
|    Decatur |                    1.4 |                            18.2 |                 54.6% |
|  Van Buren |                    0.3 |                             4.1 |                 50.1% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    1.1 |                             9.3 |               \-66.7% |
| Dickinson |                    0.7 |                             4.1 |               \-57.2% |
|    Hardin |                    0.9 |                             5.1 |               \-53.6% |
|    Monona |                    0.1 |                             1.7 |               \-46.7% |
|  Buchanan |                    0.3 |                             1.4 |               \-43.7% |
|   Johnson |                   10.3 |                             6.8 |               \-42.8% |
|  Harrison |                    0.6 |                             4.1 |               \-42.1% |
|  Delaware |                    1.3 |                             7.6 |               \-40.7% |
|    Benton |                    1.7 |                             6.7 |               \-40.6% |
|     Mills |                    0.7 |                             4.7 |               \-40.0% |
