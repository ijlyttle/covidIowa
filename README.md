Compiled at 2021-05-09 20:15:27 UTC

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

## Tables as of 2021-05-09

As of 2021-05-09, IPDH is reporting 155 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |
| 2021-05-08 |                  339.4 |                            10.8 |                \-4.4% |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   54.1 |                            11.0 |               \-16.3% |
|          Linn |                   20.0 |                             8.8 |                \-9.3% |
|         Scott |                   37.9 |                            21.9 |                \-0.7% |
|       Johnson |                   10.1 |                             6.7 |               \-47.7% |
|    Black Hawk |                    7.0 |                             5.3 |               \-34.9% |
|      Woodbury |                    6.3 |                             6.1 |               \-20.3% |
|       Dubuque |                    7.7 |                             7.9 |               \-10.3% |
|         Story |                   10.4 |                            10.7 |               \-29.2% |
|        Dallas |                   11.0 |                            11.8 |                  9.1% |
| Pottawattamie |                   11.6 |                            12.4 |               \-24.8% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Calhoun |                    3.4 |                            35.5 |                 47.6% |
| Franklin |                    3.4 |                            34.1 |                 29.2% |
| Ringgold |                    1.6 |                            32.1 |                 20.0% |
|    Davis |                    2.4 |                            27.0 |                100.1% |
|  Madison |                    3.9 |                            23.6 |                  9.7% |
|  Audubon |                    1.3 |                            23.4 |                 77.8% |
|    Scott |                   37.9 |                            21.9 |                \-0.7% |
|    Emmet |                    2.0 |                            21.7 |                  0.0% |
| Crawford |                    3.6 |                            21.2 |                128.6% |
|   Jasper |                    7.9 |                            21.1 |                121.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Crawford |                    3.6 |                            21.2 |                128.6% |
|     Jasper |                    7.9 |                            21.1 |                121.4% |
|      Davis |                    2.4 |                            27.0 |                100.1% |
|      Sioux |                    4.3 |                            12.3 |                 94.8% |
|    Audubon |                    1.3 |                            23.4 |                 77.8% |
|        Lee |                    4.1 |                            12.3 |                 71.4% |
| Washington |                    3.0 |                            13.7 |                 64.7% |
|    Decatur |                    1.4 |                            18.2 |                 54.6% |
|  Van Buren |                    0.3 |                             4.1 |                 50.1% |
|     Keokuk |                    0.7 |                             7.0 |                 50.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Union |                    1.1 |                             9.3 |               \-66.7% |
|    Harrison |                    0.4 |                             3.1 |               \-54.5% |
|   Dickinson |                    0.9 |                             5.0 |               \-53.6% |
|    Buchanan |                    0.1 |                             0.7 |               \-52.9% |
| Buena Vista |                    0.1 |                             0.7 |               \-52.9% |
|      Hardin |                    0.9 |                             5.1 |               \-48.0% |
|     Johnson |                   10.1 |                             6.7 |               \-47.7% |
|       Mills |                    0.7 |                             4.7 |               \-45.5% |
|         Ida |                  \-0.1 |                           \-2.1 |               \-45.4% |
|      Benton |                    1.6 |                             6.1 |               \-42.0% |
