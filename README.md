Compiled at 2021-05-18 20:19:58 UTC

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

## Tables as of 2021-05-18

As of 2021-05-18, IPDH is reporting 196 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-18 |                  220.4 |                             7.0 |               \-26.5% |
| 2021-05-17 |                  235.1 |                             7.5 |               \-24.2% |
| 2021-05-16 |                  237.1 |                             7.5 |               \-24.6% |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   38.3 |                             7.8 |               \-27.1% |
|          Linn |                   17.4 |                             7.7 |                \-9.8% |
|         Scott |                   20.6 |                            11.9 |               \-39.8% |
|       Johnson |                    7.0 |                             4.6 |               \-36.4% |
|    Black Hawk |                    7.4 |                             5.7 |                  0.0% |
|      Woodbury |                    4.7 |                             4.6 |               \-20.0% |
|       Dubuque |                    5.3 |                             5.4 |               \-22.8% |
|         Story |                    6.6 |                             6.8 |               \-22.1% |
|        Dallas |                    5.9 |                             6.3 |               \-33.3% |
| Pottawattamie |                    8.0 |                             8.6 |               \-24.1% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    4.0 |                            39.7 |                 20.7% |
|     Hancock |                    2.4 |                            22.9 |                 60.0% |
|  Des Moines |                    8.3 |                            21.3 |                 58.5% |
|   Muscatine |                    6.4 |                            15.1 |               \-23.5% |
|     Calhoun |                    1.4 |                            14.8 |               \-46.9% |
|       Davis |                    1.3 |                            14.3 |               \-36.0% |
|   Winnebago |                    1.4 |                            13.8 |                \-5.5% |
|       Worth |                    1.0 |                            13.5 |               \-17.7% |
| Cerro Gordo |                    5.7 |                            13.5 |                  2.2% |
|       Scott |                   20.6 |                            11.9 |               \-39.8% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Jackson |                    2.3 |                            11.8 |                 77.0% |
|     Monroe |                    0.4 |                             5.6 |                 66.7% |
|       Lyon |                    0.9 |                             7.3 |                 62.5% |
|    Hancock |                    2.4 |                            22.9 |                 60.0% |
| Des Moines |                    8.3 |                            21.3 |                 58.5% |
| Pocahontas |                    0.3 |                             4.3 |                 50.1% |
|       Iowa |                    1.1 |                             7.1 |                 50.0% |
|   Hamilton |                    1.3 |                             8.7 |                 45.5% |
|       Cass |                    1.0 |                             7.8 |                 40.0% |
|     Taylor |                    0.6 |                             9.3 |                 37.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                    1.3 |                             3.5 |               \-76.8% |
| Washington |                    0.4 |                             2.0 |               \-61.5% |
|   Crawford |                    0.6 |                             3.4 |               \-59.3% |
| Montgomery |                    0.0 |                             0.0 |               \-56.3% |
| Winneshiek |                  \-0.1 |                           \-0.7 |               \-53.9% |
|    Clayton |                    0.1 |                             0.8 |               \-52.9% |
|     Warren |                    3.4 |                             6.7 |               \-47.5% |
|    Calhoun |                    1.4 |                            14.8 |               \-46.9% |
|       Page |                    0.1 |                             0.9 |               \-46.7% |
|     Wright |                    0.9 |                             6.8 |               \-45.8% |
