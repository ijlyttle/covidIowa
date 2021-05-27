Compiled at 2021-05-27 20:31:11 UTC

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

## Tables as of 2021-05-27

As of 2021-05-27, IPDH is reporting 132 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   21.0 |                             4.3 |               \-39.8% |
|          Linn |                   10.1 |                             4.5 |               \-37.6% |
|         Scott |                    9.1 |                             5.3 |               \-41.3% |
|       Johnson |                    5.1 |                             3.4 |               \-21.8% |
|    Black Hawk |                    7.1 |                             5.4 |                \-1.7% |
|      Woodbury |                    4.4 |                             4.3 |               \-20.8% |
|       Dubuque |                    6.0 |                             6.2 |                  8.9% |
|         Story |                    4.7 |                             4.9 |                \-2.4% |
|        Dallas |                    3.6 |                             3.8 |               \-33.3% |
| Pottawattamie |                    2.6 |                             2.8 |               \-51.9% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.9 |                            15.6 |                 85.7% |
| Cerro Gordo |                    6.6 |                            15.5 |                  6.0% |
|         Ida |                    0.9 |                            12.5 |                 30.0% |
|       Worth |                    0.7 |                             9.7 |                  9.1% |
|     Jackson |                    1.9 |                             9.6 |                \-4.8% |
|       Emmet |                    0.9 |                             9.3 |                 44.4% |
|  Des Moines |                    3.4 |                             8.8 |               \-49.2% |
|     Madison |                    1.4 |                             8.7 |                 41.7% |
|         Lee |                    2.9 |                             8.5 |                 50.0% |
|     Hancock |                    0.9 |                             8.1 |               \-31.6% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                 85.7% |
|    Clayton |                    1.0 |                             5.7 |                 75.0% |
|        Lee |                    2.9 |                             8.5 |                 50.0% |
|      Jones |                    1.3 |                             6.2 |                 45.5% |
|     Benton |                    0.9 |                             3.3 |                 44.4% |
|      Emmet |                    0.9 |                             9.3 |                 44.4% |
|     Greene |                    0.4 |                             4.8 |                 42.9% |
|    Decatur |                    0.4 |                             5.5 |                 42.9% |
|    Madison |                    1.4 |                             8.7 |                 41.7% |
| Washington |                    1.1 |                             5.2 |                 36.4% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Wright |                  \-0.4 |                           \-3.4 |               \-73.4% |
|         Henry |                    0.3 |                             1.4 |               \-64.0% |
|     Palo Alto |                  \-0.1 |                           \-1.6 |               \-60.0% |
|      Franklin |                    0.7 |                             7.1 |               \-55.6% |
|        Bremer |                    0.7 |                             2.8 |               \-52.0% |
| Pottawattamie |                    2.6 |                             2.8 |               \-51.9% |
|         Floyd |                    0.3 |                             1.8 |               \-50.0% |
|    Des Moines |                    3.4 |                             8.8 |               \-49.2% |
|      Cherokee |                  \-0.1 |                           \-1.3 |               \-45.4% |
|       Guthrie |                    0.1 |                             1.3 |               \-42.8% |
