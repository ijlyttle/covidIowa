Compiled at 2021-05-19 20:18:28 UTC

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

## Tables as of 2021-05-19

As of 2021-05-19, IPDH is reporting 284 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   36.4 |                             7.4 |               \-36.6% |
|          Linn |                   16.6 |                             7.3 |               \-24.5% |
|         Scott |                   18.6 |                            10.7 |               \-50.5% |
|       Johnson |                    6.9 |                             4.5 |               \-38.9% |
|    Black Hawk |                    7.4 |                             5.7 |                \-9.2% |
|      Woodbury |                    5.6 |                             5.4 |               \-11.5% |
|       Dubuque |                    5.3 |                             5.4 |               \-24.1% |
|         Story |                    5.3 |                             5.4 |               \-46.3% |
|        Dallas |                    5.6 |                             6.0 |               \-48.3% |
| Pottawattamie |                    7.4 |                             8.0 |               \-32.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    2.7 |                            27.0 |               \-36.6% |
|  Des Moines |                    8.0 |                            20.5 |                 12.5% |
|   Muscatine |                    8.0 |                            18.8 |                 16.7% |
| Cerro Gordo |                    6.9 |                            16.2 |                 19.6% |
|       Davis |                    1.4 |                            15.9 |               \-22.7% |
|   Palo Alto |                    1.1 |                            12.9 |                 25.0% |
|     Hancock |                    1.3 |                            12.1 |               \-23.8% |
|     Jackson |                    2.3 |                            11.8 |                 43.7% |
|       Scott |                   18.6 |                            10.7 |               \-50.5% |
|     Guthrie |                    1.1 |                            10.7 |                  7.2% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Louisa |                    1.0 |                             9.1 |                 75.0% |
|   Poweshiek |                    0.9 |                             4.6 |                 44.4% |
|     Jackson |                    2.3 |                            11.8 |                 43.7% |
|   Van Buren |                    0.6 |                             8.1 |                 37.4% |
|        Lyon |                    0.7 |                             6.1 |                 33.3% |
|      Hardin |                    1.1 |                             6.8 |                 25.0% |
|   Palo Alto |                    1.1 |                            12.9 |                 25.0% |
|      Monroe |                    0.4 |                             5.6 |                 25.0% |
|   Jefferson |                    0.7 |                             3.9 |                 19.9% |
| Cerro Gordo |                    6.9 |                            16.2 |                 19.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    1.3 |                             3.5 |               \-76.5% |
| Washington |                    0.0 |                             0.0 |               \-73.1% |
|    Calhoun |                    0.6 |                             5.9 |               \-69.5% |
|        Lee |                    1.4 |                             4.2 |               \-59.5% |
|      Union |                    0.0 |                             0.0 |               \-58.8% |
|      Jones |                    0.9 |                             4.1 |               \-56.7% |
| Montgomery |                    0.0 |                             0.0 |               \-56.3% |
|  Winnebago |                    0.6 |                             5.5 |               \-54.2% |
|      Scott |                   18.6 |                            10.7 |               \-50.5% |
|     Benton |                    0.6 |                             2.2 |               \-50.0% |
