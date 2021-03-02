Compiled at 2021-03-02 17:47:58 UTC

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

## Tables as of 2021-03-02

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |
| 2021-02-25 |                  527.7 |                            16.7 |                \-3.0% |
| 2021-02-24 |                  524.0 |                            16.6 |                \-8.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   99.1 |                            20.2 |                \-7.8% |
|          Linn |                   20.7 |                             9.1 |                \-6.2% |
|         Scott |                   19.4 |                            11.2 |                \-5.3% |
|       Johnson |                   17.1 |                            11.3 |                  0.0% |
|    Black Hawk |                   13.4 |                            10.2 |                  4.1% |
|      Woodbury |                   18.7 |                            18.1 |                 14.0% |
|       Dubuque |                   18.1 |                            18.6 |                  0.8% |
|         Story |                   16.6 |                            17.1 |               \-10.9% |
|        Dallas |                   24.1 |                            25.8 |                  8.0% |
| Pottawattamie |                   14.1 |                            15.2 |                 10.4% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   17.3 |                            46.5 |                 24.3% |
|     Wapello |                   14.6 |                            41.7 |                 22.5% |
| Buena Vista |                    6.7 |                            34.2 |                125.0% |
|    Crawford |                    5.1 |                            30.6 |                 19.4% |
|      Benton |                    7.3 |                            28.4 |                 23.4% |
|        Cass |                    3.6 |                            27.8 |                 28.0% |
|     O’Brien |                    3.7 |                            27.0 |                 73.7% |
|       Lucas |                    2.3 |                            26.6 |                 64.3% |
|      Dallas |                   24.1 |                            25.8 |                  8.0% |
|       Cedar |                    4.7 |                            25.3 |               \-11.1% |

Most growth in positive tests, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    6.7 |                            34.2 |                125.0% |
|   Jefferson |                    1.6 |                             8.6 |                124.9% |
|      Bremer |                    6.0 |                            23.9 |                113.0% |
|       Emmet |                    1.4 |                            15.5 |                112.5% |
|   Winnebago |                    2.6 |                            24.8 |                 78.6% |
|         Sac |                    2.0 |                            20.6 |                 75.0% |
|     O’Brien |                    3.7 |                            27.0 |                 73.7% |
|  Pocahontas |                    0.7 |                            10.8 |                 71.4% |
|       Floyd |                    1.1 |                             7.3 |                 66.6% |
|       Lucas |                    2.3 |                            26.6 |                 64.3% |

Biggest decline in positive tests, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    2.7 |                            18.0 |               \-77.8% |
|      Adair |                    1.0 |                            14.0 |               \-57.6% |
| Washington |                    1.3 |                             5.9 |               \-46.7% |
|  Appanoose |                    1.3 |                            10.3 |               \-46.7% |
|       Lyon |                    0.9 |                             7.3 |               \-45.8% |
|     Wright |                    1.0 |                             8.0 |               \-39.1% |
|    Audubon |                    0.6 |                            10.4 |               \-38.9% |
|    Kossuth |                    2.3 |                            15.4 |               \-34.3% |
|      Wayne |                    0.4 |                             6.7 |               \-33.3% |
|     Taylor |                    0.4 |                             7.0 |               \-33.3% |
