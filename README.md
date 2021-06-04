Compiled at 2021-06-04 21:06:44 UTC

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

## Tables as of 2021-06-04

As of 2021-06-04, IPDH is reporting 112 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   12.4 |                             2.5 |               \-39.0% |
|          Linn |                    8.9 |                             3.9 |               \-11.5% |
|         Scott |                    7.9 |                             4.5 |               \-12.7% |
|       Johnson |                    4.4 |                             2.9 |               \-11.6% |
|    Black Hawk |                    7.9 |                             6.0 |                  8.8% |
|      Woodbury |                    1.6 |                             1.5 |               \-52.6% |
|       Dubuque |                    4.1 |                             4.3 |               \-26.5% |
|         Story |                    2.6 |                             2.6 |               \-37.5% |
|        Dallas |                    2.9 |                             3.1 |               \-15.6% |
| Pottawattamie |                    2.9 |                             3.1 |                  8.0% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |                \-7.7% |
|    Franklin |                    1.1 |                            11.4 |                 25.0% |
|       Davis |                    1.0 |                            11.1 |                 16.7% |
|   Winnebago |                    1.0 |                             9.7 |                 16.7% |
|      Wright |                    1.1 |                             9.1 |                275.3% |
|  Washington |                    1.9 |                             8.5 |                 33.3% |
|  Des Moines |                    3.3 |                             8.4 |                \-3.2% |
|       Adams |                    0.3 |                             7.9 |                  0.0% |
|       Emmet |                    0.7 |                             7.8 |                \-7.7% |
| Cerro Gordo |                    3.0 |                             7.1 |               \-47.2% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Wright |                    1.1 |                             9.1 |                275.3% |
| Winneshiek |                    0.9 |                             4.3 |                 85.7% |
|   Cherokee |                    0.4 |                             3.8 |                 66.7% |
|    Guthrie |                    0.7 |                             6.7 |                 50.0% |
|     Clarke |                    0.6 |                             6.1 |                 37.4% |
|     Hardin |                    1.1 |                             6.8 |                 36.4% |
|  Palo Alto |                    0.1 |                             1.6 |                 33.4% |
| Washington |                    1.9 |                             8.5 |                 33.3% |
|      Henry |                    0.7 |                             3.6 |                 33.3% |
|      Floyd |                    0.7 |                             4.6 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                  \-0.4 |                           \-2.1 |               \-63.7% |
|     Wapello |                    0.0 |                             0.0 |               \-56.3% |
|        Tama |                    0.0 |                             0.0 |               \-53.3% |
|    Woodbury |                    1.6 |                             1.5 |               \-52.6% |
| Cerro Gordo |                    3.0 |                             7.1 |               \-47.2% |
|    Delaware |                    0.0 |                             0.0 |               \-46.1% |
|     Clayton |                    0.1 |                             0.8 |               \-42.8% |
|     Jackson |                    0.7 |                             3.7 |               \-40.0% |
|        Polk |                   12.4 |                             2.5 |               \-39.0% |
|        Iowa |                    0.1 |                             0.9 |               \-38.4% |
