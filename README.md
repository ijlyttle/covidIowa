Compiled at 2021-03-01 20:49:42 UTC

<!-- README.md is generated from README.Rmd. Please edit that file -->

# covidIowa

<!-- badges: start -->

<!-- badges: end -->

The goal of this repository is to give a county-level summary of
COVID-19 cases in Iowa. The data is taken from a series of daily
snapshots of the [accessibility
page](https://coronavirus.iowa.gov/pages/access) provided by the Iowa
Department of Public Health.

I think that, for this dataset, **cases** means positive *tests*, not
positive *individuals*, as this
[comment](https://github.com/nytimes/covid-19-data/issues/546#issuecomment-784247266)
by the NYT data team indicates. All I know is that small numbers are
good and big numbers are bad.

If you want to work with the data yourself, all the code I use is
published this repository, check out the [`workflow`](workflow)
directory. Processed datasets are also available here:

  - [`iowa_county_meta.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_meta.csv):
    county metadata, things like estimated 2019 population from
    [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
    at Iowa State University.

  - [`iowa_county_data.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    daily numbers by county from IDPH, going back to 2020-05-25.

  - [`iowa_county_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    In addition to county metadata, total positive-tests (and per 100k),
    one week average of daily positive-tests (and per 100k), and
    week-over-week change in positive tests (as a ratio).

  - [`iowa_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    Similar to `iowa_county_cases_week.csv`, but aggregated for the
    entire state.

## Plots

![](workflow/data/99-publish/iowa_cases.png)

![](workflow/data/99-publish/iowa_change.png)

## Tables as of 2021-03-01

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |
| 2021-02-25 |                  527.7 |                            16.7 |                \-3.0% |
| 2021-02-24 |                  524.0 |                            16.6 |                \-8.8% |
| 2021-02-23 |                  510.1 |                            16.2 |               \-19.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  109.1 |                            22.3 |                  1.7% |
|          Linn |                   22.6 |                            10.0 |                  3.1% |
|         Scott |                   21.0 |                            12.1 |                  1.3% |
|       Johnson |                   18.9 |                            12.5 |                 11.2% |
|    Black Hawk |                   13.9 |                            10.6 |                 14.3% |
|      Woodbury |                   18.4 |                            17.9 |                  7.1% |
|       Dubuque |                   20.1 |                            20.7 |                 23.3% |
|         Story |                   19.3 |                            19.9 |                 12.7% |
|        Dallas |                   25.0 |                            26.8 |                 14.5% |
| Pottawattamie |                   15.0 |                            16.1 |                  9.8% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   17.3 |                            46.5 |               \-20.0% |
|     Wapello |                   14.9 |                            42.5 |                 15.6% |
| Buena Vista |                    6.9 |                            34.9 |                120.0% |
|       Cedar |                    5.7 |                            30.7 |                 23.7% |
|    Crawford |                    5.0 |                            29.7 |                 20.0% |
|      Benton |                    7.1 |                            27.9 |                  9.6% |
|      Dallas |                   25.0 |                            26.8 |                 14.5% |
|   Appanoose |                    3.3 |                            26.4 |                 57.9% |
|     Osceola |                    1.6 |                            26.4 |                 28.6% |
|      Monroe |                    1.9 |                            24.1 |                 42.8% |

Most growth in positive tests, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    6.9 |                            34.9 |                120.0% |
|        Tama |                    3.9 |                            22.9 |                100.0% |
|   Jefferson |                    1.6 |                             8.6 |                 79.9% |
|       Mills |                    2.3 |                            15.1 |                 77.0% |
|      Bremer |                    5.7 |                            22.8 |                 74.1% |
|   Appanoose |                    3.3 |                            26.4 |                 57.9% |
|     O’Brien |                    3.0 |                            21.8 |                 55.6% |
|   Allamakee |                    3.1 |                            23.0 |                 52.7% |
|     Mahaska |                    2.7 |                            12.3 |                 44.5% |
|        Iowa |                    2.7 |                            16.8 |                 44.5% |

Biggest decline in positive tests, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    2.3 |                            15.1 |               \-82.7% |
| Washington |                    1.3 |                             5.9 |               \-55.6% |
|       Clay |                    0.6 |                             3.6 |               \-54.2% |
|      Adair |                    1.4 |                            20.0 |               \-51.4% |
|    Audubon |                    0.6 |                            10.4 |               \-45.0% |
|      Wayne |                    0.3 |                             4.4 |               \-43.7% |
|     Taylor |                    0.3 |                             4.7 |               \-43.7% |
|   Cherokee |                    0.7 |                             6.4 |               \-42.9% |
|   Hamilton |                    1.3 |                             8.7 |               \-42.8% |
|  Van Buren |                    0.1 |                             2.0 |               \-38.4% |
