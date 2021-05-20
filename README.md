Compiled at 2021-05-20 20:18:41 UTC

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

## Tables as of 2021-05-20

As of 2021-05-20, IPDH is reporting 233 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   35.6 |                             7.3 |               \-20.2% |
|          Linn |                   16.9 |                             7.4 |                \-4.6% |
|         Scott |                   16.3 |                             9.4 |               \-49.2% |
|       Johnson |                    6.9 |                             4.5 |               \-24.7% |
|    Black Hawk |                    7.3 |                             5.6 |                  5.5% |
|      Woodbury |                    5.9 |                             5.7 |                 20.0% |
|       Dubuque |                    5.4 |                             5.6 |                \-6.2% |
|         Story |                    4.9 |                             5.0 |               \-45.3% |
|        Dallas |                    5.9 |                             6.3 |               \-36.8% |
| Pottawattamie |                    6.4 |                             6.9 |               \-31.6% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    2.9 |                            28.4 |               \-25.0% |
|  Des Moines |                    7.7 |                            19.8 |                 29.8% |
|     Hancock |                    1.7 |                            16.1 |                \-5.0% |
|       Davis |                    1.4 |                            15.9 |                  0.0% |
| Cerro Gordo |                    6.1 |                            14.5 |                 11.1% |
|       Henry |                    2.6 |                            12.9 |                108.3% |
|   Palo Alto |                    1.1 |                            12.9 |                 15.4% |
|   Muscatine |                    4.7 |                            11.0 |               \-39.4% |
|       Boone |                    2.9 |                            10.9 |                  3.9% |
|     Jackson |                    2.0 |                            10.3 |                 31.2% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Henry |                    2.6 |                            12.9 |                108.3% |
|  Poweshiek |                    0.9 |                             4.6 |                 62.5% |
|  Appanoose |                    0.6 |                             4.6 |                 57.1% |
|     Louisa |                    0.9 |                             7.8 |                 44.4% |
|  Van Buren |                    0.4 |                             6.1 |                 42.9% |
|        Ida |                    0.4 |                             6.3 |                 42.9% |
|    Jackson |                    2.0 |                            10.3 |                 31.2% |
|  Jefferson |                    0.9 |                             4.7 |                 30.0% |
| Des Moines |                    7.7 |                            19.8 |                 29.8% |
|     Bremer |                    2.6 |                            10.3 |                 25.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    1.4 |                             3.8 |               \-71.2% |
|    Calhoun |                    0.4 |                             4.4 |               \-64.3% |
|      Jones |                    0.6 |                             2.8 |               \-59.3% |
|     Benton |                    0.3 |                             1.1 |               \-57.1% |
|   Crawford |                    0.7 |                             4.2 |               \-55.6% |
|  Winnebago |                    0.6 |                             5.5 |               \-52.2% |
|    Madison |                    0.7 |                             4.4 |               \-50.0% |
|      Scott |                   16.3 |                             9.4 |               \-49.2% |
|        Lee |                    1.6 |                             4.7 |               \-47.1% |
| Montgomery |                    0.0 |                             0.0 |               \-46.1% |
