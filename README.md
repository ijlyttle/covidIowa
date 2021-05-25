Compiled at 2021-05-25 20:21:19 UTC

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

## Tables as of 2021-05-25

As of 2021-05-25, IPDH is reporting 169 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   26.9 |                             5.5 |               \-29.1% |
|          Linn |                   11.1 |                             4.9 |               \-34.1% |
|         Scott |                   12.7 |                             7.4 |               \-36.4% |
|       Johnson |                    5.3 |                             3.5 |               \-21.4% |
|    Black Hawk |                    7.9 |                             6.0 |                  5.1% |
|      Woodbury |                    5.4 |                             5.3 |                 12.5% |
|       Dubuque |                    5.1 |                             5.3 |                \-2.3% |
|         Story |                    5.1 |                             5.3 |               \-18.9% |
|        Dallas |                    6.3 |                             6.7 |                  6.3% |
| Pottawattamie |                    3.6 |                             3.8 |               \-49.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Cerro Gordo |                    7.4 |                            17.5 |                 25.5% |
|    Franklin |                    1.4 |                            14.2 |               \-51.4% |
|  Des Moines |                    5.3 |                            13.6 |               \-32.3% |
|     Audubon |                    0.7 |                            13.0 |                 33.3% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|      Louisa |                    1.3 |                            11.7 |                100.0% |
|       Adair |                    0.7 |                            10.0 |                 33.3% |
|   Palo Alto |                    0.9 |                             9.6 |                  8.3% |
|     Madison |                    1.6 |                             9.6 |                  5.8% |
|       Davis |                    0.9 |                             9.5 |               \-18.8% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Louisa |                    1.3 |                            11.7 |                100.0% |
|  Poweshiek |                    1.6 |                             8.5 |                 99.9% |
|    Clayton |                    1.0 |                             5.7 |                 75.0% |
|       Page |                    1.0 |                             6.6 |                 75.0% |
| Washington |                    1.4 |                             6.5 |                 70.0% |
| Winneshiek |                    0.4 |                             2.1 |                 66.7% |
|    O’Brien |                    0.7 |                             5.2 |                 50.0% |
|   Crawford |                    1.3 |                             7.6 |                 45.5% |
|      Adams |                    0.4 |                            11.9 |                 42.9% |
|      Union |                    0.7 |                             5.8 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Calhoun |                    0.1 |                             1.5 |               \-52.9% |
|      Franklin |                    1.4 |                            14.2 |               \-51.4% |
| Pottawattamie |                    3.6 |                             3.8 |               \-49.2% |
|        Marion |                    0.9 |                             2.6 |               \-48.0% |
|      Buchanan |                    0.1 |                             0.7 |               \-46.7% |
|       Hancock |                    1.0 |                             9.4 |               \-41.7% |
|     Winnebago |                    0.4 |                             4.1 |               \-41.2% |
|      Hamilton |                    0.4 |                             2.9 |               \-37.5% |
|     Muscatine |                    3.7 |                             8.7 |               \-36.5% |
|         Scott |                   12.7 |                             7.4 |               \-36.4% |
