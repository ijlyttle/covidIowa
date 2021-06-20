Compiled at 2021-06-20 16:58:22 UTC

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

## Tables as of 2021-06-19

As of 2021-06-19, IPDH is reporting 136 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-19 |                   83.4 |                             2.6 |                  1.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.7 |                             2.4 |               \-19.1% |
|          Linn |                    6.9 |                             3.0 |               \-15.4% |
|         Scott |                    3.3 |                             1.9 |                  0.0% |
|       Johnson |                    2.4 |                             1.6 |                \-7.7% |
|    Black Hawk |                   15.1 |                            11.5 |                 27.0% |
|      Woodbury |                    1.7 |                             1.7 |               \-17.4% |
|       Dubuque |                    2.1 |                             2.2 |               \-21.4% |
|         Story |                    1.1 |                             1.2 |                \-6.3% |
|        Dallas |                    0.7 |                             0.8 |               \-50.0% |
| Pottawattamie |                    2.3 |                             2.5 |                \-4.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.9 |                            15.6 |                \-7.2% |
|  Black Hawk |                   15.1 |                            11.5 |                 27.0% |
|  Winneshiek |                    1.6 |                             7.9 |                 99.9% |
|      Benton |                    2.0 |                             7.8 |                109.9% |
|    Buchanan |                    1.4 |                             6.7 |                 21.5% |
| Cerro Gordo |                    2.7 |                             6.4 |                 44.5% |
| Buena Vista |                    1.1 |                             5.8 |                 66.6% |
|       Mills |                    0.9 |                             5.7 |                 30.0% |
|       Floyd |                    0.9 |                             5.5 |                 18.2% |
|     Hancock |                    0.6 |                             5.4 |                 37.4% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Henry |                    0.7 |                             3.6 |                140.1% |
|    Crawford |                    0.9 |                             5.1 |                116.7% |
|      Benton |                    2.0 |                             7.8 |                109.9% |
|    Marshall |                    1.0 |                             2.5 |                100.0% |
|  Winneshiek |                    1.6 |                             7.9 |                 99.9% |
| Buena Vista |                    1.1 |                             5.8 |                 66.6% |
|      Butler |                    0.6 |                             4.0 |                 57.1% |
| Cerro Gordo |                    2.7 |                             6.4 |                 44.5% |
|      Wright |                    0.4 |                             3.4 |                 42.9% |
|      Keokuk |                    0.4 |                             4.2 |                 42.9% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Dallas |                    0.7 |                             0.8 |               \-50.0% |
|     Page |                    0.0 |                             0.0 |               \-50.0% |
| Hamilton |                    0.3 |                             1.9 |               \-35.7% |
|    Emmet |                  \-0.1 |                           \-1.6 |               \-33.4% |
|   Warren |                    1.0 |                             1.9 |               \-33.3% |
|  Clinton |                    0.3 |                             0.6 |               \-30.7% |
|  Jackson |                    0.0 |                             0.0 |               \-30.0% |
|   Marion |                    0.1 |                             0.4 |               \-27.2% |
|  Clayton |                    0.1 |                             0.8 |               \-27.2% |
|    Union |                    0.1 |                             1.2 |               \-27.2% |
