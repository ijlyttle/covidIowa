Compiled at 2021-07-22 20:16:04 UTC

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

## Tables as of 2021-07-21

As of 2021-07-21, IPDH is reporting -4515 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-21 |                \-491.9 |                          \-15.6 |              \-470.7% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                 \-91.4 |                          \-18.7 |              \-300.3% |
|          Linn |                 \-42.1 |                          \-18.6 |              \-409.7% |
|         Scott |                 \-17.1 |                           \-9.9 |              \-397.3% |
|       Johnson |                 \-14.1 |                           \-9.4 |              \-378.8% |
|    Black Hawk |                 \-82.4 |                          \-62.8 |              \-454.0% |
|      Woodbury |                  \-8.3 |                           \-8.0 |              \-609.9% |
|       Dubuque |                 \-14.7 |                          \-15.1 |              \-346.2% |
|         Story |                 \-12.1 |                          \-12.5 |              \-234.5% |
|        Dallas |                 \-18.6 |                          \-19.9 |              \-232.3% |
| Pottawattamie |                 \-11.0 |                          \-11.8 |              \-391.6% |

Most positive-cases, per-capita:

    #> Warning: One or more parsing issues, see `problems()` for details

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Appanoose |                    2.0 |                            16.1 |              \-333.3% |
|      Iowa |                    2.6 |                            15.9 |              \-266.6% |
|     Lucas |                    1.1 |                            13.3 |              \-849.3% |
|   Carroll |                    1.0 |                             5.0 |              \-300.0% |
|   Mahaska |                    0.9 |                             3.9 |              \-176.5% |
|     Worth |                    0.1 |                             1.9 |              \-899.3% |
|   Osceola |                    0.0 |                             0.0 |                 16.7% |
|     Union |                  \-0.1 |                           \-1.2 |                    NA |
|     Jones |                  \-0.3 |                           \-1.4 |                 25.0% |
|    Shelby |                  \-0.3 |                           \-2.5 |              \-349.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Adams |                  \-0.1 |                           \-4.0 |                 99.8% |
|     Jones |                  \-0.3 |                           \-1.4 |                 25.0% |
|   Osceola |                    0.0 |                             0.0 |                 16.7% |
|  Ringgold |                  \-0.7 |                          \-14.6 |               \-49.9% |
|    Howard |                  \-0.6 |                           \-6.2 |               \-62.5% |
| Van Buren |                  \-0.6 |                           \-8.1 |               \-62.5% |
|  Delaware |                  \-0.7 |                           \-4.2 |               \-71.4% |
|    Taylor |                  \-0.7 |                          \-11.7 |               \-75.0% |
|  Mitchell |                  \-0.9 |                           \-8.1 |               \-90.9% |
|      Cass |                  \-0.9 |                           \-6.7 |               \-91.7% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|    Winneshiek |                  \-3.7 |                          \-18.6 |            \-1 049.0% |
|         Worth |                    0.1 |                             1.9 |              \-899.3% |
|         Lucas |                    1.1 |                            13.3 |              \-849.3% |
|      Woodbury |                  \-8.3 |                           \-8.0 |              \-609.9% |
|    Black Hawk |                 \-82.4 |                          \-62.8 |              \-454.0% |
|          Linn |                 \-42.1 |                          \-18.6 |              \-409.7% |
|        Benton |                  \-5.9 |                          \-22.8 |              \-409.2% |
|         Scott |                 \-17.1 |                           \-9.9 |              \-397.3% |
| Pottawattamie |                 \-11.0 |                          \-11.8 |              \-391.6% |
|           Lee |                 \-11.0 |                          \-32.7 |              \-391.6% |
