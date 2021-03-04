Compiled at 2021-03-04 20:55:34 UTC

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

## Tables as of 2021-03-04

I believe these numbers refer to positive tests, not to newly-reported
positive individuals.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-04 |                  501.0 |                            15.9 |                \-5.1% |
| 2021-03-03 |                  498.6 |                            15.8 |                \-4.8% |
| 2021-03-02 |                  512.0 |                            16.2 |                  0.4% |
| 2021-03-01 |                  535.6 |                            17.0 |                  8.4% |
| 2021-02-28 |                  534.0 |                            16.9 |                  7.6% |
| 2021-02-27 |                  540.1 |                            17.1 |                  6.7% |
| 2021-02-26 |                  540.4 |                            17.1 |                  4.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   96.0 |                            19.6 |               \-10.1% |
|          Linn |                   19.6 |                             8.6 |               \-14.3% |
|         Scott |                   18.7 |                            10.8 |                \-0.7% |
|       Johnson |                   17.1 |                            11.3 |                \-3.8% |
|    Black Hawk |                   13.1 |                            10.0 |               \-13.2% |
|      Woodbury |                   18.6 |                            18.0 |                \-0.7% |
|       Dubuque |                   13.0 |                            13.4 |               \-36.8% |
|         Story |                   19.3 |                            19.9 |                  6.8% |
|        Dallas |                   22.3 |                            23.8 |                \-1.8% |
| Pottawattamie |                   11.3 |                            12.1 |               \-21.8% |

Most positive-tests, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   16.7 |                            44.9 |                 31.9% |
|     O’Brien |                    5.9 |                            42.6 |                118.2% |
|     Wapello |                   12.4 |                            35.5 |                \-3.1% |
|   Allamakee |                    4.6 |                            33.4 |                160.0% |
|        Cass |                    4.1 |                            32.3 |                 33.3% |
|      Bremer |                    7.6 |                            30.2 |                185.7% |
| Buena Vista |                    5.9 |                            29.9 |                 41.2% |
|      Shelby |                    3.3 |                            28.7 |                 57.9% |
|       Lucas |                    2.1 |                            24.9 |                 37.5% |
|    Crawford |                    4.1 |                            24.6 |               \-10.0% |

Most growth in positive tests, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Bremer |                    7.6 |                            30.2 |                185.7% |
| Allamakee |                    4.6 |                            33.4 |                160.0% |
|  Mitchell |                    2.0 |                            18.9 |                133.3% |
|   O’Brien |                    5.9 |                            42.6 |                118.2% |
| Jefferson |                    2.0 |                            10.9 |                109.9% |
| Chickasaw |                    2.0 |                            16.8 |                 91.0% |
|  Humboldt |                    2.1 |                            22.4 |                 83.4% |
|   Fayette |                    3.1 |                            16.0 |                 81.2% |
|    Butler |                    2.0 |                            13.9 |                 75.0% |
|       Ida |                    1.1 |                            16.7 |                 66.6% |

Biggest decline in positive tests, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Page |                    2.9 |                            18.9 |               \-75.5% |
|     Adair |                    0.6 |                             8.0 |               \-57.7% |
|    Louisa |                    0.6 |                             5.2 |               \-54.2% |
|  Hamilton |                    0.7 |                             4.8 |               \-53.9% |
|    Howard |                    0.7 |                             7.8 |               \-53.9% |
|     Henry |                    1.0 |                             5.0 |               \-44.0% |
| Appanoose |                    1.4 |                            11.5 |               \-43.3% |
|      Lyon |                    0.9 |                             7.3 |               \-38.1% |
|   Clinton |                    6.6 |                            14.2 |               \-37.7% |
|       Lee |                    3.6 |                            10.6 |               \-37.3% |
