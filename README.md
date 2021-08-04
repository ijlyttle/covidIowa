Compiled at 2021-08-04 20:19:24 UTC

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

## Tables as of 2021-07-28

As of 2021-07-28, IPDH is reporting -1.274510^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-28 |               \-1649.3 |                          \-52.3 |            \-1 272.6% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                \-284.3 |                          \-58.0 |            \-1 579.8% |
|          Linn |                \-121.4 |                          \-53.6 |            \-1 786.0% |
|         Scott |                \-131.7 |                          \-76.2 |            \-1 967.3% |
|       Johnson |                 \-56.9 |                          \-37.6 |            \-1 877.2% |
|    Black Hawk |                \-125.0 |                          \-95.3 |              \-823.3% |
|      Woodbury |                 \-36.3 |                          \-35.2 |              \-688.1% |
|       Dubuque |                 \-45.1 |                          \-46.4 |            \-1 645.1% |
|         Story |                 \-48.3 |                          \-49.7 |            \-1 755.1% |
|        Dallas |                 \-53.6 |                          \-57.3 |            \-1 326.6% |
| Pottawattamie |                 \-49.1 |                          \-52.7 |            \-1 223.3% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Appanoose |                  \-0.1 |                           \-1.2 |               \-14.3% |
|      Iowa |                  \-0.7 |                           \-4.4 |               \-71.4% |
|     Lucas |                  \-1.4 |                          \-16.6 |              \-133.4% |
| Jefferson |                  \-3.4 |                          \-18.7 |              \-241.7% |
|    Howard |                  \-1.9 |                          \-20.3 |              \-175.0% |
|   Carroll |                  \-4.1 |                          \-20.5 |              \-300.1% |
|  Mitchell |                  \-2.4 |                          \-22.9 |              \-171.4% |
| Van Buren |                  \-1.7 |                          \-24.3 |              \-171.4% |
|   O’Brien |                  \-3.4 |                          \-24.9 |              \-288.9% |
|    Shelby |                  \-2.9 |                          \-24.9 |              \-186.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Appanoose |                  \-0.1 |                           \-1.2 |               \-14.3% |
|      Iowa |                  \-0.7 |                           \-4.4 |               \-71.4% |
|     Lucas |                  \-1.4 |                          \-16.6 |              \-133.4% |
|     Adams |                  \-1.7 |                          \-47.6 |              \-141.7% |
|  Mitchell |                  \-2.4 |                          \-22.9 |              \-171.4% |
| Van Buren |                  \-1.7 |                          \-24.3 |              \-171.4% |
|    Howard |                  \-1.9 |                          \-20.3 |              \-175.0% |
|    Shelby |                  \-2.9 |                          \-24.9 |              \-186.7% |
|    Taylor |                  \-2.1 |                          \-35.0 |              \-214.3% |
|   Osceola |                  \-2.1 |                          \-36.0 |              \-214.3% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                 \-58.0 |                         \-156.0 |            \-2 593.4% |
|   Muscatine |                 \-33.1 |                          \-77.7 |            \-1 975.3% |
|       Scott |                \-131.7 |                          \-76.2 |            \-1 967.3% |
|     Johnson |                 \-56.9 |                          \-37.6 |            \-1 877.2% |
|        Linn |                \-121.4 |                          \-53.6 |            \-1 786.0% |
|       Story |                 \-48.3 |                          \-49.7 |            \-1 755.1% |
|     Dubuque |                 \-45.1 |                          \-46.4 |            \-1 645.1% |
|        Polk |                \-284.3 |                          \-58.0 |            \-1 579.8% |
| Cerro Gordo |                 \-42.0 |                          \-98.9 |            \-1 535.1% |
|       Henry |                 \-16.9 |                          \-84.5 |            \-1 333.0% |
