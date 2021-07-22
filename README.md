Compiled at 2021-07-22 17:27:12 UTC

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

As of 2021-07-21, IPDH is reporting -1.242110^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-21 |               \-1621.3 |                          \-51.4 |            \-1 323.5% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                \-279.9 |                          \-57.1 |              \-717.7% |
|          Linn |                \-120.1 |                          \-53.0 |              \-996.8% |
|         Scott |                \-130.6 |                          \-75.5 |            \-2 486.6% |
|       Johnson |                 \-56.6 |                          \-37.4 |            \-1 278.9% |
|    Black Hawk |                \-122.6 |                          \-93.4 |              \-628.6% |
|      Woodbury |                 \-35.3 |                          \-34.2 |            \-2 499.3% |
|       Dubuque |                 \-44.9 |                          \-46.1 |              \-887.2% |
|         Story |                 \-47.9 |                          \-49.3 |              \-665.5% |
|        Dallas |                 \-53.1 |                          \-56.9 |              \-492.5% |
| Pottawattamie |                 \-48.7 |                          \-52.3 |            \-1 491.5% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Appanoose |                  \-0.1 |                           \-1.2 |              \-166.6% |
|      Iowa |                  \-0.7 |                           \-4.4 |              \-113.3% |
|     Lucas |                  \-1.1 |                          \-13.3 |               \-50.0% |
|    Howard |                  \-1.7 |                          \-18.7 |              \-162.5% |
| Jefferson |                  \-3.4 |                          \-18.7 |              \-270.0% |
|   Carroll |                  \-4.1 |                          \-20.5 |                214.3% |
|  Mitchell |                  \-2.3 |                          \-21.6 |              \-181.9% |
|    Shelby |                  \-2.6 |                          \-22.4 |                449.3% |
|   O’Brien |                  \-3.3 |                          \-23.9 |              \-194.1% |
| Van Buren |                  \-1.7 |                          \-24.3 |              \-162.5% |

Most growth in positive cases, week-over-week:

    #> Warning: One or more parsing issues, see `problems()` for details

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                  \-4.6 |                          \-83.2 |              2 397.2% |
|      Worth |                  \-3.9 |                          \-52.3 |              1 897.9% |
|     Shelby |                  \-2.6 |                          \-22.4 |                449.3% |
|    Carroll |                  \-4.1 |                          \-20.5 |                214.3% |
|    Mahaska |                  \-7.0 |                          \-31.7 |                147.0% |
|      Lucas |                  \-1.1 |                          \-13.3 |               \-50.0% |
|       Iowa |                  \-0.7 |                           \-4.4 |              \-113.3% |
| Pocahontas |                  \-2.3 |                          \-34.5 |              \-160.0% |
|     Howard |                  \-1.7 |                          \-18.7 |              \-162.5% |
|  Van Buren |                  \-1.7 |                          \-24.3 |              \-162.5% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|      Woodbury |                 \-35.3 |                          \-34.2 |            \-2 499.3% |
|         Scott |                \-130.6 |                          \-75.5 |            \-2 486.6% |
|    Winneshiek |                  \-6.4 |                          \-32.2 |            \-1 998.3% |
|     Muscatine |                 \-32.9 |                          \-77.0 |            \-1 586.6% |
| Pottawattamie |                 \-48.7 |                          \-52.3 |            \-1 491.5% |
|         Jones |                  \-8.7 |                          \-42.1 |            \-1 451.0% |
|       Johnson |                 \-56.6 |                          \-37.4 |            \-1 278.9% |
|       Clinton |                 \-25.0 |                          \-53.8 |            \-1 033.5% |
|          Linn |                \-120.1 |                          \-53.0 |              \-996.8% |
|        Benton |                 \-13.6 |                          \-52.9 |              \-900.2% |
