Compiled at 2021-03-04 20:51:47 UTC

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

-   [`iowa_county_meta.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_meta.csv):
    county metadata, things like estimated 2019 population from
    [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
    at Iowa State University.

-   [`iowa_county_data.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_data.csv):
    daily numbers by county from IDPH, going back to 2020-05-25.

-   [`iowa_county_cases_week.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_county_data.csv):
    In addition to county metadata, total positive-tests (and per 100k),
    one week average of daily positive-tests (and per 100k), and
    week-over-week change in positive tests (as a ratio).

-   [`iowa_cases_week.csv`](https://raw.githubusercontent.com/ijlyttle/covidIowa/master/workflow/data/99-publish/iowa_cases_week.csv):
    Similar to `iowa_county_cases_week.csv`, but aggregated for the
    entire state.

## Plots

![](workflow/data/99-publish/iowa_cases.png)

![](workflow/data/99-publish/iowa_change.png)

## Tables as of 2021-03-04

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|-----------:|-----------------------:|--------------------------------:|----------------------:|
| 2021-03-04 |                  405.1 |                            12.8 |                -23.2% |
| 2021-03-03 |                  498.6 |                            15.8 |                 -4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|--------------:|-----------------------:|--------------------------------:|----------------------:|
|          Polk |                   77.0 |                            15.7 |                -27.7% |
|          Linn |                   16.1 |                             7.1 |                -28.6% |
|         Scott |                   15.1 |                             8.8 |                -18.7% |
|       Johnson |                   14.0 |                             9.3 |                -20.5% |
|    Black Hawk |                    9.6 |                             7.3 |                -35.1% |
|      Woodbury |                   14.9 |                            14.4 |                -19.6% |
|       Dubuque |                   11.0 |                            11.3 |                -45.8% |
|         Story |                   16.3 |                            16.8 |                 -9.0% |
|        Dallas |                   18.0 |                            19.3 |                -19.9% |
| Pottawattamie |                    9.3 |                            10.0 |                -34.5% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|------------:|-----------------------:|--------------------------------:|----------------------:|
|      Jasper |                   15.7 |                            42.3 |                 24.5% |
|     O’Brien |                    4.7 |                            34.3 |                 81.8% |
|     Wapello |                   10.9 |                            31.0 |                -14.4% |
|   Allamakee |                    4.1 |                            30.3 |                140.0% |
|        Cass |                    3.9 |                            30.0 |                 25.9% |
| Buena Vista |                    5.4 |                            27.7 |                 32.4% |
|      Bremer |                    6.1 |                            24.5 |                138.1% |
|       Cedar |                    4.0 |                            21.5 |                -20.5% |
|   Winnebago |                    2.1 |                            20.7 |                 15.8% |
|       Lucas |                    1.7 |                            19.9 |                 18.7% |

Most growth in positive tests, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|----------:|-----------------------:|--------------------------------:|----------------------:|
| Allamakee |                    4.1 |                            30.3 |                140.0% |
|    Bremer |                    6.1 |                            24.5 |                138.1% |
|  Mitchell |                    1.7 |                            16.2 |                111.0% |
| Jefferson |                    1.9 |                            10.2 |                 99.9% |
|   O’Brien |                    4.7 |                            34.3 |                 81.8% |
|       Ida |                    1.0 |                            14.6 |                 55.5% |
|    Butler |                    1.6 |                            10.9 |                 50.0% |
|  Humboldt |                    1.6 |                            16.4 |                 50.0% |
| Van Buren |                    0.4 |                             6.1 |                 42.9% |
|     Davis |                    1.4 |                            15.9 |                 41.7% |

Biggest decline in positive tests, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
|-----------:|-----------------------:|--------------------------------:|----------------------:|
|       Page |                    2.4 |                            16.1 |                -78.2% |
|      Henry |                    0.3 |                             1.4 |                -64.0% |
|     Howard |                    0.6 |                             6.2 |                -57.7% |
|      Adair |                    0.6 |                             8.0 |                -57.7% |
|     Louisa |                    0.6 |                             5.2 |                -54.2% |
|    Clinton |                    4.7 |                            10.2 |                -52.9% |
|    Kossuth |                    1.6 |                            10.6 |                -50.0% |
|   Hamilton |                    0.9 |                             5.8 |                -50.0% |
|  Appanoose |                    1.1 |                             9.2 |                -50.0% |
| Washington |                    0.7 |                             3.3 |                -47.8% |
