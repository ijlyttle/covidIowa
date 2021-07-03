Compiled at 2021-07-03 17:21:51 UTC

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

## Tables as of 2021-07-03

As of 2021-07-03, IPDH is reporting 76 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   10.6 |                             2.2 |                 80.0% |
|          Linn |                    5.1 |                             2.3 |                \-6.5% |
|         Scott |                    3.0 |                             1.7 |                 55.6% |
|       Johnson |                    1.9 |                             1.2 |                \-9.1% |
|    Black Hawk |                   12.6 |                             9.6 |               \-18.8% |
|      Woodbury |                    2.1 |                             2.1 |                100.1% |
|       Dubuque |                    2.3 |                             2.3 |                 15.0% |
|         Story |                    1.0 |                             1.0 |               \-12.5% |
|        Dallas |                    1.1 |                             1.2 |               \-11.8% |
| Pottawattamie |                    1.7 |                             1.8 |                 11.7% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Wayne |                    1.0 |                            15.5 |                100.0% |
|   Humboldt |                    1.4 |                            15.0 |                112.5% |
|    Webster |                    4.9 |                            13.5 |                 36.7% |
|    Decatur |                    0.9 |                            10.9 |                 62.5% |
| Black Hawk |                   12.6 |                             9.6 |               \-18.8% |
| Winneshiek |                    1.9 |                             9.3 |                 53.9% |
|   Ringgold |                    0.4 |                             8.8 |                 42.9% |
|        Lee |                    2.9 |                             8.5 |                 35.0% |
|      Adams |                    0.3 |                             7.9 |                  0.0% |
|   Crawford |                    1.3 |                             7.6 |                128.6% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Crawford |                    1.3 |                             7.6 |                128.6% |
|      Warren |                    1.9 |                             3.6 |                122.2% |
|    Humboldt |                    1.4 |                            15.0 |                112.5% |
|    Woodbury |                    2.1 |                             2.1 |                100.1% |
|     Carroll |                    0.4 |                             2.1 |                100.1% |
|       Wayne |                    1.0 |                            15.5 |                100.0% |
| Cerro Gordo |                    2.1 |                             5.0 |                 83.4% |
|        Polk |                   10.6 |                             2.2 |                 80.0% |
|      Hardin |                    1.3 |                             7.6 |                 77.8% |
|    Franklin |                    0.7 |                             7.1 |                 71.4% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monona |                    0.0 |                             0.0 |               \-50.0% |
| Buchanan |                    0.0 |                             0.0 |               \-41.7% |
|    Sioux |                    0.1 |                             0.4 |               \-33.3% |
| Marshall |                    1.1 |                             2.9 |               \-31.8% |
|  Fayette |                    0.3 |                             1.5 |               \-30.7% |
|    Adair |                    0.0 |                             0.0 |               \-30.0% |
|  O’Brien |                  \-0.1 |                           \-1.0 |               \-25.0% |
|   Benton |                    1.0 |                             3.9 |               \-22.2% |
|     Iowa |                    0.0 |                             0.0 |               \-22.2% |
|   Howard |                    0.0 |                             0.0 |               \-22.2% |
