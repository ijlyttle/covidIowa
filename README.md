Compiled at 2021-06-06 17:44:58 UTC

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

## Tables as of 2021-06-06

As of 2021-06-06, IPDH is reporting 78 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   13.4 |                             2.7 |               \-15.8% |
|          Linn |                   11.7 |                             5.2 |                 34.8% |
|         Scott |                    7.3 |                             4.2 |               \-12.1% |
|       Johnson |                    3.7 |                             2.5 |               \-28.3% |
|    Black Hawk |                    8.7 |                             6.6 |                 28.3% |
|      Woodbury |                    1.9 |                             1.8 |               \-39.4% |
|       Dubuque |                    4.1 |                             4.3 |               \-21.7% |
|         Story |                    1.9 |                             1.9 |               \-35.5% |
|        Dallas |                    3.6 |                             3.8 |                 68.4% |
| Pottawattamie |                    3.3 |                             3.5 |                 76.5% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    0.9 |                            15.6 |                 44.4% |
|   Franklin |                    1.0 |                             9.9 |                 16.7% |
|  Winnebago |                    1.0 |                             9.7 |                  7.7% |
|     Wright |                    1.0 |                             8.0 |                366.2% |
| Washington |                    1.7 |                             7.8 |                 72.8% |
|      Emmet |                    0.7 |                             7.8 |                  0.0% |
| Des Moines |                    2.7 |                             7.0 |                \-7.2% |
|    Guthrie |                    0.7 |                             6.7 |                 71.4% |
| Black Hawk |                    8.7 |                             6.6 |                 28.3% |
|        Ida |                    0.4 |                             6.3 |               \-28.6% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Wright |                    1.0 |                             8.0 |                366.2% |
| Pottawattamie |                    3.3 |                             3.5 |                 76.5% |
|         Henry |                    1.0 |                             5.0 |                 75.0% |
|    Washington |                    1.7 |                             7.8 |                 72.8% |
|       Guthrie |                    0.7 |                             6.7 |                 71.4% |
|        Dallas |                    3.6 |                             3.8 |                 68.4% |
|       Carroll |                    0.3 |                             1.4 |                 50.1% |
|       Fayette |                    0.9 |                             4.4 |                 44.4% |
|       Audubon |                    0.9 |                            15.6 |                 44.4% |
|        Benton |                    1.1 |                             4.5 |                 36.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Louisa |                  \-0.1 |                           \-1.3 |               \-57.2% |
| Cerro Gordo |                    1.9 |                             4.4 |               \-53.5% |
|       Jones |                    0.3 |                             1.4 |               \-50.0% |
|        Iowa |                  \-0.1 |                           \-0.9 |               \-50.0% |
|      Shelby |                  \-0.4 |                           \-3.7 |               \-50.0% |
|     Mahaska |                    0.1 |                             0.6 |               \-46.7% |
|      Jasper |                    0.0 |                             0.0 |               \-41.7% |
|   Poweshiek |                    0.3 |                             1.5 |               \-40.0% |
|    Woodbury |                    1.9 |                             1.8 |               \-39.4% |
|    Buchanan |                    0.1 |                             0.7 |               \-38.4% |
