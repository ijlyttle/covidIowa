Compiled at 2021-05-21 20:18:20 UTC

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

## Tables as of 2021-05-21

As of 2021-05-21, IPDH is reporting 176 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |
| 2021-05-19 |                  207.6 |                             6.6 |               \-37.7% |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   32.0 |                             6.5 |               \-26.2% |
|          Linn |                   14.4 |                             6.4 |               \-12.2% |
|         Scott |                   15.4 |                             8.9 |               \-43.9% |
|       Johnson |                    5.7 |                             3.8 |               \-29.9% |
|    Black Hawk |                    6.4 |                             4.9 |                \-8.8% |
|      Woodbury |                    5.9 |                             5.7 |                 17.1% |
|       Dubuque |                    4.7 |                             4.8 |               \-11.1% |
|         Story |                    5.4 |                             5.6 |               \-25.0% |
|        Dallas |                    6.1 |                             6.6 |               \-19.4% |
| Pottawattamie |                    5.9 |                             6.3 |               \-34.3% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    2.0 |                            19.9 |               \-44.7% |
|  Des Moines |                    6.7 |                            17.2 |                  1.9% |
| Cerro Gordo |                    6.7 |                            15.8 |                 28.6% |
|     Hancock |                    1.6 |                            14.8 |               \-18.2% |
|       Davis |                    1.3 |                            14.3 |                \-5.9% |
|       Boone |                    3.3 |                            12.5 |                 25.0% |
|       Adams |                    0.4 |                            11.9 |                 42.9% |
|   Palo Alto |                    1.0 |                            11.3 |                 16.7% |
|       Henry |                    2.1 |                            10.7 |                 37.5% |
|     Guthrie |                    1.1 |                            10.7 |                  7.2% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|  Poweshiek |                    1.4 |                             7.7 |                142.9% |
| Washington |                    1.9 |                             8.5 |                122.2% |
|  Appanoose |                    0.6 |                             4.6 |                 57.1% |
|    Clayton |                    0.9 |                             4.9 |                 44.4% |
|    Fremont |                    0.4 |                             6.2 |                 42.9% |
|      Adams |                    0.4 |                            11.9 |                 42.9% |
|      Henry |                    2.1 |                            10.7 |                 37.5% |
|     Monona |                    0.1 |                             1.7 |                 33.4% |
|  Jefferson |                    0.7 |                             3.9 |                 33.3% |
|    Carroll |                    1.4 |                             7.1 |                 30.8% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    1.1 |                             3.1 |               \-73.2% |
|    Calhoun |                    0.4 |                             4.4 |               \-56.5% |
|      Jones |                    0.7 |                             3.5 |               \-50.0% |
|     Benton |                    0.4 |                             1.7 |               \-47.3% |
|    Osceola |                    0.1 |                             2.4 |               \-46.7% |
|  Muscatine |                    4.1 |                             9.7 |               \-45.5% |
|   Franklin |                    2.0 |                            19.9 |               \-44.7% |
|      Scott |                   15.4 |                             8.9 |               \-43.9% |
|   Plymouth |                    0.3 |                             1.1 |               \-40.0% |
| Winneshiek |                  \-0.1 |                           \-0.7 |               \-40.0% |
