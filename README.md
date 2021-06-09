Compiled at 2021-06-09 17:11:52 UTC

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

## Tables as of 2021-06-09

As of 2021-06-09, IPDH is reporting 109 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |
| 2021-06-07 |                   97.7 |                             3.1 |               \-10.1% |
| 2021-06-06 |                  100.6 |                             3.2 |               \-13.7% |
| 2021-06-05 |                  101.6 |                             3.2 |               \-21.0% |
| 2021-06-04 |                  100.3 |                             3.2 |               \-28.1% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   18.1 |                             3.7 |                 47.3% |
|          Linn |                   12.9 |                             5.7 |                 86.5% |
|         Scott |                    5.4 |                             3.1 |               \-28.6% |
|       Johnson |                    3.3 |                             2.2 |               \-11.8% |
|    Black Hawk |                   11.9 |                             9.0 |                125.0% |
|      Woodbury |                    2.1 |                             2.1 |                \-8.3% |
|       Dubuque |                    4.3 |                             4.4 |                 15.6% |
|         Story |                    2.0 |                             2.1 |               \-19.2% |
|        Dallas |                    3.9 |                             4.1 |                100.0% |
| Pottawattamie |                    4.3 |                             4.6 |                208.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Audubon |                    1.7 |                            31.2 |                137.4% |
|   Franklin |                    1.0 |                             9.9 |                 40.0% |
|       Page |                    1.4 |                             9.5 |                112.5% |
|      Emmet |                    0.9 |                             9.3 |                 18.2% |
| Black Hawk |                   11.9 |                             9.0 |                125.0% |
|  Winnebago |                    0.9 |                             8.3 |                \-7.2% |
|        Lee |                    2.7 |                             8.1 |                 62.5% |
|      Union |                    0.9 |                             7.0 |                 18.2% |
| Des Moines |                    2.7 |                             7.0 |                 13.0% |
| Washington |                    1.3 |                             5.9 |                 45.5% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
| Pottawattamie |                    4.3 |                             4.6 |                208.4% |
|       Audubon |                    1.7 |                            31.2 |                137.4% |
|    Black Hawk |                   11.9 |                             9.0 |                125.0% |
|          Page |                    1.4 |                             9.5 |                112.5% |
|        Dallas |                    3.9 |                             4.1 |                100.0% |
|          Linn |                   12.9 |                             5.7 |                 86.5% |
|           Lee |                    2.7 |                             8.1 |                 62.5% |
|       Fayette |                    0.9 |                             4.4 |                 62.5% |
|        Warren |                    2.1 |                             4.2 |                 57.1% |
|         Cedar |                    0.6 |                             3.1 |                 57.1% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Jones |                    0.0 |                             0.0 |               \-50.0% |
|      Keokuk |                  \-0.3 |                           \-2.8 |               \-50.0% |
|    Marshall |                    0.3 |                             0.7 |               \-43.7% |
|       Henry |                    0.1 |                             0.7 |               \-38.4% |
|       Davis |                    0.3 |                             3.2 |               \-35.7% |
| Cerro Gordo |                    2.4 |                             5.7 |               \-33.3% |
|         Ida |                    0.1 |                             2.1 |               \-33.3% |
|       Boone |                    0.6 |                             2.2 |               \-31.3% |
|   Poweshiek |                    0.3 |                             1.5 |               \-30.7% |
|   Muscatine |                    1.3 |                             3.0 |               \-30.4% |
