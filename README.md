Compiled at 2021-02-28 23:24:58 UTC

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

-   [`iowa_county_meta.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_meta.csv):
    county metadata, things like estimated 2019 population from
    [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
    at Iowa State University.
-   [`iowa_county_data.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    daily numbers by county from IDPH, going back to 2020-05-25.
-   [`iowa_county_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    In addition to county metadata, total cases (and per 100k), one week
    averages of new cases (and per 100k), and week-over-week change in
    cases (as a ratio).
-   [`iowa_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    Similar to `iowa_county_cases_week.csv`, but aggregated for the
    entire state.

## Plots

![](workflow/data/99-publish/iowa_cases.png)

![](workflow/data/99-publish/iowa_change.png)

## Tables as of 2021-02-28

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|-----------:|-----------------------:|--------------------------------:|----------------------:|
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |
| 2021-02-25 |                  527.7 |                            16.7 |                 -3.0% |
| 2021-02-24 |                  524.0 |                            16.6 |                 -8.8% |
| 2021-02-23 |                  510.1 |                            16.2 |                -19.4% |
| 2021-02-22 |                  494.0 |                            15.7 |                -25.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|--------------:|-----------------------:|--------------------------------:|----------------------:|
|          Polk |                  107.4 |                            21.9 |                 -1.3% |
|          Linn |                   21.9 |                             9.6 |                 -2.4% |
|         Scott |                   21.0 |                            12.1 |                 -3.7% |
|       Johnson |                   18.1 |                            12.0 |                  2.3% |
|    Black Hawk |                   13.7 |                            10.5 |                 15.7% |
|      Woodbury |                   18.6 |                            18.0 |                  3.8% |
|       Dubuque |                   19.1 |                            19.7 |                 18.5% |
|         Story |                   18.7 |                            19.3 |                 10.4% |
|        Dallas |                   25.3 |                            27.1 |                 16.5% |
| Pottawattamie |                   14.7 |                            15.8 |                 10.0% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|------------:|-----------------------:|--------------------------------:|----------------------:|
|      Jasper |                   18.0 |                            48.4 |                -16.9% |
|     Wapello |                   14.9 |                            42.5 |                 22.0% |
|        Page |                    5.9 |                            38.8 |                -56.0% |
| Buena Vista |                    6.6 |                            33.5 |                103.9% |
|    Crawford |                    4.9 |                            28.9 |                 24.2% |
|       Cedar |                    5.3 |                            28.4 |                 18.9% |
|      Dallas |                   25.3 |                            27.1 |                 16.5% |
|      Benton |                    6.9 |                            26.7 |                 -5.2% |
|     Osceola |                    1.6 |                            26.4 |                 28.6% |
|      Clarke |                    2.4 |                            25.9 |                -17.2% |

Most growth in positive-tests, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|------------:|-----------------------:|--------------------------------:|----------------------:|
| Buena Vista |                    6.6 |                            33.5 |                103.9% |
|    Harrison |                    2.4 |                            17.3 |                 71.4% |
|        Tama |                    3.4 |                            20.3 |                 63.2% |
|      Bremer |                    5.3 |                            21.1 |                 63.0% |
|       Mills |                    2.0 |                            13.2 |                 61.6% |
|      Hardin |                    3.6 |                            21.2 |                 60.0% |
|       Floyd |                    1.0 |                             6.4 |                 55.5% |
|   Jefferson |                    1.6 |                             8.6 |                 50.0% |
|  Pocahontas |                    0.4 |                             6.5 |                 42.9% |
|     O’Brien |                    2.7 |                            19.7 |                 36.8% |

Biggest decline in positive-tests, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|-----------:|-----------------------:|--------------------------------:|----------------------:|
| Washington |                    1.3 |                             5.9 |                -61.0% |
|      Adair |                    1.6 |                            22.0 |                -57.2% |
|       Page |                    5.9 |                            38.8 |                -56.0% |
|     Taylor |                    0.3 |                             4.7 |                -43.7% |
|   Cherokee |                    0.7 |                             6.4 |                -42.9% |
|   Hamilton |                    1.4 |                             9.7 |                -41.4% |
|       Clay |                    0.9 |                             5.4 |                -40.9% |
|   Marshall |                    4.1 |                            10.5 |                -37.9% |
|     Howard |                    1.1 |                            12.5 |                -37.5% |
|    Audubon |                    0.7 |                            13.0 |                -36.8% |
