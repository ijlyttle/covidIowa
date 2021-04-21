Compiled at 2021-04-21 00:00:41 UTC

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

## Tables as of 2021-04-20

As of 2021-04-20, IPDH is reporting 549 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |
| 2021-04-14 |                  497.0 |                            15.8 |                \-8.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   76.0 |                            15.5 |               \-16.9% |
|          Linn |                   26.4 |                            11.7 |                  3.2% |
|         Scott |                   57.0 |                            33.0 |                \-4.9% |
|       Johnson |                   30.6 |                            20.2 |                  7.3% |
|    Black Hawk |                   15.6 |                            11.9 |                \-8.7% |
|      Woodbury |                   18.3 |                            17.7 |                \-6.2% |
|       Dubuque |                   19.0 |                            19.5 |               \-25.1% |
|         Story |                   11.3 |                            11.6 |               \-17.3% |
|        Dallas |                   11.3 |                            12.1 |               \-16.5% |
| Pottawattamie |                   21.0 |                            22.5 |               \-13.5% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    3.0 |                            50.4 |                 21.7% |
|     Dickinson |                    5.7 |                            33.1 |               \-25.4% |
|         Scott |                   57.0 |                            33.0 |                \-4.9% |
|         Emmet |                    2.9 |                            31.0 |                \-3.6% |
|           Sac |                    2.6 |                            26.4 |                 47.0% |
|        Shelby |                    3.0 |                            26.2 |                \-9.7% |
|          Clay |                    4.1 |                            25.9 |               \-21.7% |
| Pottawattamie |                   21.0 |                            22.5 |               \-13.5% |
|     Palo Alto |                    2.0 |                            22.5 |                \-4.5% |
|        Warren |                   11.4 |                            22.2 |                  6.1% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Pocahontas |                    1.1 |                            17.3 |                114.3% |
|     Monona |                    1.4 |                            16.6 |                 70.0% |
|      Adair |                    1.1 |                            16.0 |                 66.6% |
|     Benton |                    2.3 |                             8.9 |                 64.3% |
|    Madison |                    2.9 |                            17.5 |                 50.0% |
|    Webster |                    3.0 |                             8.4 |                 47.4% |
|        Sac |                    2.6 |                            26.4 |                 47.0% |
|    Guthrie |                    1.6 |                            14.7 |                 38.4% |
|  Jefferson |                    0.6 |                             3.1 |                 37.4% |
|   Hamilton |                    1.7 |                            11.6 |                 35.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-0.9 |                           \-7.0 |               \-94.1% |
| Washington |                    0.7 |                             3.3 |               \-64.7% |
|    Wapello |                    1.0 |                             2.9 |               \-44.0% |
|       Page |                    1.0 |                             6.6 |               \-41.7% |
|      Davis |                    0.0 |                             0.0 |               \-41.7% |
|   Crawford |                    0.7 |                             4.2 |               \-40.0% |
|    Fremont |                    0.9 |                            12.3 |               \-38.1% |
|     Jasper |                    1.6 |                             4.2 |               \-33.3% |
|      Mills |                    1.6 |                            10.4 |               \-33.3% |
|    Mahaska |                    2.3 |                            10.3 |               \-32.3% |
