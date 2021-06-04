Compiled at 2021-06-04 00:47:16 UTC

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

## Tables as of 2021-06-02

As of 2021-06-02, IPDH is reporting 275 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.6 |                             2.4 |               \-51.6% |
|          Linn |                    8.9 |                             3.9 |               \-17.9% |
|         Scott |                    9.0 |                             5.2 |               \-16.7% |
|       Johnson |                    3.7 |                             2.5 |               \-25.0% |
|    Black Hawk |                    7.6 |                             5.8 |                  3.4% |
|      Woodbury |                    2.7 |                             2.6 |               \-25.7% |
|       Dubuque |                    3.6 |                             3.7 |               \-38.5% |
|         Story |                    2.6 |                             2.6 |               \-41.9% |
|        Dallas |                    2.6 |                             2.8 |               \-34.2% |
| Pottawattamie |                    2.4 |                             2.6 |               \-11.1% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Adams |                    0.4 |                            11.9 |                 11.1% |
|       Davis |                    1.0 |                            11.1 |                 16.7% |
|   Winnebago |                    1.1 |                            11.0 |                 36.4% |
|     Audubon |                    0.6 |                            10.4 |                \-8.3% |
|       Emmet |                    0.9 |                             9.3 |                  8.3% |
|         Ida |                    0.6 |                             8.3 |                  0.0% |
|   Van Buren |                    0.6 |                             8.1 |                 83.3% |
| Cerro Gordo |                    3.3 |                             7.7 |               \-46.4% |
|  Des Moines |                    3.0 |                             7.7 |               \-12.5% |
|   Muscatine |                    2.9 |                             6.7 |                 28.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|  Van Buren |                    0.6 |                             8.1 |                 83.3% |
|     Bremer |                    1.6 |                             6.3 |                 79.9% |
|   Cherokee |                    0.4 |                             3.8 |                 66.7% |
|    Webster |                    1.1 |                             3.2 |                 50.0% |
|     Wright |                    0.7 |                             5.7 |                 50.0% |
|     Shelby |                    0.0 |                             0.0 |                 40.1% |
| Winneshiek |                    0.6 |                             2.9 |                 37.4% |
|    Fayette |                    0.6 |                             2.9 |                 37.4% |
|     Clarke |                    0.6 |                             6.1 |                 37.4% |
|     Benton |                    1.1 |                             4.5 |                 36.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     O’Brien |                  \-0.4 |                           \-3.1 |               \-63.7% |
|        Tama |                    0.0 |                             0.0 |               \-56.3% |
|       Boone |                    0.6 |                             2.2 |               \-56.0% |
|    Delaware |                    0.0 |                             0.0 |               \-53.3% |
|        Polk |                   11.6 |                             2.4 |               \-51.6% |
|     Madison |                    0.4 |                             2.6 |               \-50.0% |
|       Cedar |                    0.1 |                             0.8 |               \-46.7% |
|     Clayton |                    0.1 |                             0.8 |               \-46.7% |
|     Hancock |                    0.1 |                             1.3 |               \-46.7% |
| Cerro Gordo |                    3.3 |                             7.7 |               \-46.4% |
