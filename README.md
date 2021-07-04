Compiled at 2021-07-04 17:21:59 UTC

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

## Tables as of 2021-07-04

As of 2021-07-04, IPDH is reporting 61 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   10.3 |                             2.1 |                 61.2% |
|          Linn |                    4.6 |                             2.0 |               \-26.4% |
|         Scott |                    3.1 |                             1.8 |                 61.1% |
|       Johnson |                    1.6 |                             1.0 |                \-5.3% |
|    Black Hawk |                   13.0 |                             9.9 |                \-9.3% |
|      Woodbury |                    2.3 |                             2.2 |                 77.0% |
|       Dubuque |                    2.0 |                             2.1 |               \-12.5% |
|         Story |                    1.0 |                             1.0 |               \-12.5% |
|        Dallas |                    1.3 |                             1.4 |                  6.7% |
| Pottawattamie |                    2.0 |                             2.1 |                 50.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Wayne |                    1.0 |                            15.5 |                100.0% |
|   Humboldt |                    1.4 |                            15.0 |                112.5% |
|    Webster |                    4.9 |                            13.5 |                 28.1% |
| Black Hawk |                   13.0 |                             9.9 |                \-9.3% |
|    Decatur |                    0.7 |                             9.1 |                 33.3% |
|   Ringgold |                    0.4 |                             8.8 |                 42.9% |
|        Lee |                    2.7 |                             8.1 |                 23.8% |
|      Adams |                    0.3 |                             7.9 |               \-10.0% |
|   Crawford |                    1.3 |                             7.6 |                300.4% |
|    Calhoun |                    0.7 |                             7.4 |                 50.0% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Crawford |                    1.3 |                             7.6 |                300.4% |
|  Humboldt |                    1.4 |                            15.0 |                112.5% |
|     Wayne |                    1.0 |                            15.5 |                100.0% |
| Jefferson |                    0.9 |                             4.7 |                 85.7% |
|  Plymouth |                    0.6 |                             2.3 |                 83.3% |
|  Woodbury |                    2.3 |                             2.2 |                 77.0% |
|    Warren |                    1.7 |                             3.3 |                 72.8% |
| Dickinson |                    0.7 |                             4.1 |                 71.4% |
|    Hardin |                    1.1 |                             6.8 |                 66.6% |
|      Polk |                   10.3 |                             2.1 |                 61.2% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Monona |                    0.0 |                             0.0 |               \-50.0% |
|    Keokuk |                    0.0 |                             0.0 |               \-41.7% |
|  Buchanan |                    0.0 |                             0.0 |               \-30.0% |
|     Adair |                    0.0 |                             0.0 |               \-30.0% |
|      Linn |                    4.6 |                             2.0 |               \-26.4% |
|   O’Brien |                  \-0.1 |                           \-1.0 |               \-25.0% |
| Poweshiek |                    0.0 |                             0.0 |               \-22.2% |
|      Lyon |                    0.6 |                             4.9 |               \-21.5% |
|  Marshall |                    1.1 |                             2.9 |               \-21.0% |
|     Sioux |                    0.1 |                             0.4 |               \-20.0% |
