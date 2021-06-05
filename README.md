Compiled at 2021-06-05 17:48:24 UTC

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

## Tables as of 2021-06-05

As of 2021-06-05, IPDH is reporting 108 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   13.1 |                             2.7 |               \-27.2% |
|          Linn |                   10.1 |                             4.5 |                \-3.7% |
|         Scott |                    7.9 |                             4.5 |               \-10.1% |
|       Johnson |                    3.9 |                             2.6 |               \-22.7% |
|    Black Hawk |                    8.3 |                             6.3 |                  3.2% |
|      Woodbury |                    2.0 |                             1.9 |               \-36.4% |
|       Dubuque |                    4.1 |                             4.3 |               \-23.4% |
|         Story |                    1.7 |                             1.8 |               \-51.3% |
|        Dallas |                    3.3 |                             3.5 |                 15.4% |
| Pottawattamie |                    2.6 |                             2.8 |                 25.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.7 |                            13.0 |                 33.3% |
|      Davis |                    1.1 |                            12.7 |                 36.4% |
|   Franklin |                    1.0 |                             9.9 |                 16.7% |
|  Winnebago |                    1.0 |                             9.7 |                 16.7% |
| Des Moines |                    3.3 |                             8.4 |                 15.4% |
|     Wright |                    1.0 |                             8.0 |                366.2% |
| Washington |                    1.7 |                             7.8 |                137.4% |
|      Emmet |                    0.7 |                             7.8 |                \-7.7% |
|    Guthrie |                    0.7 |                             6.7 |                 71.4% |
|      Henry |                    1.3 |                             6.4 |                128.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Wright |                    1.0 |                             8.0 |                366.2% |
| Washington |                    1.7 |                             7.8 |                137.4% |
|      Henry |                    1.3 |                             6.4 |                128.6% |
|    Guthrie |                    0.7 |                             6.7 |                 71.4% |
|     Benton |                    1.3 |                             5.0 |                 45.5% |
|    Fayette |                    0.9 |                             4.4 |                 44.4% |
|       Cass |                    0.4 |                             3.3 |                 42.9% |
|       Lyon |                    0.4 |                             3.6 |                 42.9% |
|     Clarke |                    0.6 |                             6.1 |                 37.4% |
|      Davis |                    1.1 |                            12.7 |                 36.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Cerro Gordo |                    1.9 |                             4.4 |               \-62.3% |
|       Story |                    1.7 |                             1.8 |               \-51.3% |
|     Carroll |                  \-0.3 |                           \-1.4 |               \-50.0% |
|     Wapello |                    0.3 |                             0.8 |               \-40.0% |
|     Jackson |                    0.7 |                             3.7 |               \-40.0% |
|    Plymouth |                    0.4 |                             1.7 |               \-37.5% |
|    Woodbury |                    2.0 |                             1.9 |               \-36.4% |
|      Jasper |                    0.0 |                             0.0 |               \-36.3% |
|    Delaware |                    0.0 |                             0.0 |               \-36.3% |
|       Lucas |                    0.0 |                             0.0 |               \-36.3% |
