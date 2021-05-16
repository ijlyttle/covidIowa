Compiled at 2021-05-16 17:14:00 UTC

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

## Tables as of 2021-05-16

As of 2021-05-16, IPDH is reporting 136 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   41.3 |                             8.4 |               \-23.3% |
|          Linn |                   18.0 |                             7.9 |                \-9.5% |
|         Scott |                   23.6 |                            13.6 |               \-36.8% |
|       Johnson |                    8.0 |                             5.3 |               \-19.2% |
|    Black Hawk |                    7.4 |                             5.7 |                  5.4% |
|      Woodbury |                    5.1 |                             5.0 |               \-15.7% |
|       Dubuque |                    4.9 |                             5.0 |               \-32.8% |
|         Story |                    6.4 |                             6.6 |               \-35.0% |
|        Dallas |                    5.7 |                             6.1 |               \-44.0% |
| Pottawattamie |                    8.6 |                             9.2 |               \-23.9% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Franklin |                    3.9 |                            38.3 |                  9.7% |
| Des Moines |                    8.1 |                            20.9 |                 56.1% |
|    Hancock |                    2.0 |                            18.8 |                 23.5% |
|    Calhoun |                    1.7 |                            17.7 |               \-38.7% |
|  Muscatine |                    7.1 |                            16.7 |               \-10.9% |
|      Davis |                    1.4 |                            15.9 |               \-29.2% |
|    Osceola |                    0.9 |                            14.4 |                  0.0% |
|  Winnebago |                    1.4 |                            13.8 |               \-10.5% |
|      Scott |                   23.6 |                            13.6 |               \-36.8% |
|      Worth |                    1.0 |                            13.5 |               \-12.5% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Buchanan |                    1.4 |                             6.7 |                112.5% |
| Buena Vista |                    1.0 |                             5.1 |                 75.0% |
|    Hamilton |                    1.4 |                             9.7 |                 70.0% |
|  Des Moines |                    8.1 |                            20.9 |                 56.1% |
|    Mitchell |                    0.9 |                             8.1 |                 44.4% |
|      Louisa |                    0.4 |                             3.9 |                 42.9% |
|        Cass |                    1.3 |                            10.0 |                 33.4% |
|         Ida |                    0.1 |                             2.1 |                 33.4% |
|      Monroe |                    0.3 |                             3.7 |                 28.6% |
|      Marion |                    3.1 |                             9.5 |                 26.1% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Crawford |                    0.4 |                             2.6 |               \-68.7% |
| Washington |                    0.6 |                             2.6 |               \-60.7% |
|     Jasper |                    2.6 |                             6.9 |               \-59.7% |
| Winneshiek |                    0.0 |                             0.0 |               \-56.3% |
|      Emmet |                    0.4 |                             4.7 |               \-52.4% |
|     Wright |                    0.7 |                             5.7 |               \-52.0% |
|       Page |                    0.1 |                             0.9 |               \-50.0% |
|      Sioux |                    1.7 |                             4.9 |               \-48.7% |
|    Decatur |                    0.3 |                             3.6 |               \-47.1% |
| Montgomery |                    0.1 |                             1.4 |               \-46.7% |
