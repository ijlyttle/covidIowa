Compiled at 2021-07-06 23:53:39 UTC

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

## Tables as of 2021-07-06

As of 2021-07-06, IPDH is reporting 55 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    9.1 |                             1.9 |                 22.4% |
|          Linn |                    3.6 |                             1.6 |               \-34.7% |
|         Scott |                    2.4 |                             1.4 |                  4.4% |
|       Johnson |                    1.9 |                             1.2 |                  0.0% |
|    Black Hawk |                   11.6 |                             8.8 |               \-19.3% |
|      Woodbury |                    2.3 |                             2.2 |                 64.3% |
|       Dubuque |                    1.1 |                             1.2 |               \-40.0% |
|         Story |                    1.0 |                             1.0 |               \-12.5% |
|        Dallas |                    0.7 |                             0.8 |                \-7.7% |
| Pottawattamie |                    1.6 |                             1.7 |                 38.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    6.0 |                            16.7 |                 53.1% |
|      Wayne |                    0.9 |                            13.3 |                 62.5% |
|   Humboldt |                    1.1 |                            12.0 |                 36.4% |
|    Audubon |                    0.6 |                            10.4 |                120.0% |
|    Calhoun |                    1.0 |                            10.3 |                 55.5% |
|   Franklin |                    1.0 |                             9.9 |                 75.0% |
| Black Hawk |                   11.6 |                             8.8 |               \-19.3% |
|   Ringgold |                    0.4 |                             8.8 |                 42.9% |
|        Lee |                    2.7 |                             8.1 |                 23.8% |
| Des Moines |                    2.6 |                             6.6 |                 47.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.6 |                            10.4 |                120.0% |
|   Palo Alto |                    0.3 |                             3.2 |                 80.1% |
|    Franklin |                    1.0 |                             9.9 |                 75.0% |
|    Crawford |                    0.7 |                             4.2 |                 71.4% |
|    Woodbury |                    2.3 |                             2.2 |                 64.3% |
|       Wayne |                    0.9 |                            13.3 |                 62.5% |
|      Jasper |                    1.3 |                             3.5 |                 60.0% |
| Cerro Gordo |                    2.1 |                             5.0 |                 57.1% |
|    Plymouth |                    0.6 |                             2.3 |                 57.1% |
|     Calhoun |                    1.0 |                            10.3 |                 55.5% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Cherokee |                    0.0 |                             0.0 |               \-46.1% |
|    Dubuque |                    1.1 |                             1.2 |               \-40.0% |
|     Wright |                    0.1 |                             1.1 |               \-38.4% |
| Washington |                    0.0 |                             0.0 |               \-36.3% |
|     Monona |                    0.0 |                             0.0 |               \-36.3% |
|   Marshall |                    0.9 |                             2.2 |               \-35.0% |
|       Linn |                    3.6 |                             1.6 |               \-34.7% |
|     Keokuk |                  \-0.1 |                           \-1.4 |               \-33.4% |
|       Lyon |                    0.4 |                             3.6 |               \-33.3% |
|      Adams |                    0.1 |                             4.0 |               \-27.2% |
