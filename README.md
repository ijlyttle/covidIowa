Compiled at 2021-03-03 17:53:58 UTC

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

## Tables as of 2021-03-03

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |
| 2021-02-25 |                  527.7 |                            16.7 |                \-3.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   94.6 |                            19.3 |               \-13.9% |
|          Linn |                   20.1 |                             8.9 |               \-11.9% |
|         Scott |                   18.6 |                            10.7 |                \-2.1% |
|       Johnson |                   17.6 |                            11.6 |                  2.4% |
|    Black Hawk |                   12.7 |                             9.7 |                \-5.0% |
|      Woodbury |                   18.9 |                            18.3 |                 12.1% |
|       Dubuque |                   15.7 |                            16.1 |               \-21.5% |
|         Story |                   18.3 |                            18.8 |                  0.0% |
|        Dallas |                   23.1 |                            24.8 |                 11.2% |
| Pottawattamie |                   14.3 |                            15.3 |                 16.3% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   17.1 |                            46.1 |                 28.3% |
|     O’Brien |                    5.4 |                            39.5 |                136.9% |
|     Wapello |                   13.3 |                            38.0 |                  3.1% |
|        Cass |                    4.4 |                            34.5 |                 65.2% |
|   Allamakee |                    4.3 |                            31.3 |                117.6% |
| Buena Vista |                    6.0 |                            30.6 |                 32.4% |
|       Cedar |                    5.1 |                            27.6 |                  0.0% |
|      Bremer |                    6.7 |                            26.8 |                145.4% |
|      Benton |                    6.4 |                            25.1 |                  6.1% |
|      Dallas |                   23.1 |                            24.8 |                 11.2% |

Most growth in positive tests, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Jefferson |                    2.1 |                            11.7 |                175.0% |
|    Bremer |                    6.7 |                            26.8 |                145.4% |
|   O’Brien |                    5.4 |                            39.5 |                136.9% |
| Allamakee |                    4.3 |                            31.3 |                117.6% |
|  Mitchell |                    1.7 |                            16.2 |                 72.8% |
|     Worth |                    1.7 |                            23.2 |                 72.8% |
|      Cass |                    4.4 |                            34.5 |                 65.2% |
|  Humboldt |                    1.7 |                            17.9 |                 58.3% |
|   Webster |                    6.7 |                            18.7 |                 54.3% |
|    Butler |                    2.0 |                            13.9 |                 50.0% |

Biggest decline in positive tests, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Page |                    2.9 |                            18.9 |               \-77.3% |
|     Louisa |                    0.7 |                             6.5 |               \-57.2% |
|  Appanoose |                    1.0 |                             8.0 |               \-56.2% |
|     Howard |                    0.7 |                             7.8 |               \-53.9% |
|      Henry |                    0.7 |                             3.6 |               \-50.0% |
|    Clinton |                    5.4 |                            11.7 |               \-46.4% |
|    Kossuth |                    2.0 |                            13.5 |               \-44.7% |
|       Lyon |                    1.0 |                             8.5 |               \-41.7% |
| Washington |                    1.3 |                             5.9 |               \-40.7% |
|      Adair |                    1.3 |                            18.0 |               \-38.4% |
