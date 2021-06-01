Compiled at 2021-06-01 00:52:14 UTC

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

## Tables as of 2021-05-31

As of 2021-05-31, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   14.0 |                             2.9 |               \-51.4% |
|          Linn |                    7.3 |                             3.2 |               \-31.8% |
|         Scott |                    9.1 |                             5.3 |               \-26.0% |
|       Johnson |                    4.6 |                             3.0 |               \-11.4% |
|    Black Hawk |                    5.7 |                             4.4 |               \-20.3% |
|      Woodbury |                    2.9 |                             2.8 |               \-32.5% |
|       Dubuque |                    4.1 |                             4.3 |                \-7.7% |
|         Story |                    3.1 |                             3.2 |               \-32.6% |
|        Dallas |                    2.0 |                             2.1 |               \-58.8% |
| Pottawattamie |                    0.9 |                             0.9 |               \-62.9% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Davis |                    1.1 |                            12.7 |                 15.4% |
|       Adams |                    0.4 |                            11.9 |                  0.0% |
| Cerro Gordo |                    4.7 |                            11.1 |               \-31.0% |
|         Ida |                    0.7 |                            10.4 |                 19.9% |
|   Winnebago |                    1.0 |                             9.7 |                 40.0% |
|       Jones |                    1.7 |                             8.3 |                 58.3% |
|   Poweshiek |                    1.3 |                             7.0 |                  6.7% |
|  Des Moines |                    2.4 |                             6.2 |               \-46.7% |
|       Emmet |                    0.6 |                             6.2 |                  0.0% |
|   Van Buren |                    0.4 |                             6.1 |                 42.9% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Buchanan |                    0.9 |                             4.0 |                 62.5% |
|     Jones |                    1.7 |                             8.3 |                 58.3% |
|    Greene |                    0.4 |                             4.8 |                 42.9% |
| Van Buren |                    0.4 |                             6.1 |                 42.9% |
| Winnebago |                    1.0 |                             9.7 |                 40.0% |
|  Hamilton |                    0.7 |                             4.8 |                 33.3% |
|       Sac |                    0.4 |                             4.4 |                 25.0% |
|      Iowa |                    0.7 |                             4.4 |                 19.9% |
|       Ida |                    0.7 |                            10.4 |                 19.9% |
|     Davis |                    1.1 |                            12.7 |                 15.4% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Hardin |                  \-0.1 |                           \-0.8 |               \-66.7% |
| Pottawattamie |                    0.9 |                             0.9 |               \-62.9% |
|     Allamakee |                  \-0.1 |                           \-1.0 |               \-60.0% |
|        Dallas |                    2.0 |                             2.1 |               \-58.8% |
|       Hancock |                    0.0 |                             0.0 |               \-58.8% |
|       Madison |                    0.3 |                             1.8 |               \-52.6% |
|      Franklin |                    0.4 |                             4.3 |               \-52.4% |
|        Warren |                    1.0 |                             1.9 |               \-51.7% |
|          Polk |                   14.0 |                             2.9 |               \-51.4% |
|         Henry |                    0.6 |                             2.9 |               \-50.0% |
