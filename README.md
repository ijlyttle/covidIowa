Compiled at 2021-05-01 20:22:13 UTC

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

## Tables as of 2021-05-01

As of 2021-05-01, IPDH is reporting 388 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |
| 2021-04-25 |                  418.9 |                            13.3 |                \-4.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   61.7 |                            12.6 |               \-30.4% |
|          Linn |                   19.6 |                             8.6 |               \-32.4% |
|         Scott |                   37.0 |                            21.4 |               \-20.8% |
|       Johnson |                   18.9 |                            12.5 |               \-33.8% |
|    Black Hawk |                   10.3 |                             7.8 |               \-32.5% |
|      Woodbury |                    8.4 |                             8.2 |               \-46.8% |
|       Dubuque |                    8.9 |                             9.1 |               \-35.5% |
|         Story |                   14.1 |                            14.6 |                \-1.9% |
|        Dallas |                    9.9 |                            10.5 |               \-32.1% |
| Pottawattamie |                   14.9 |                            15.9 |               \-34.7% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Union |                    4.7 |                            38.5 |              3 895.8% |
|   Winnebago |                    2.9 |                            27.6 |               \-12.9% |
|       Worth |                    2.0 |                            27.1 |                 23.5% |
|    Franklin |                    2.7 |                            27.0 |                 44.5% |
|       Adams |                    0.9 |                            23.8 |                 30.0% |
|    Ringgold |                    1.1 |                            23.4 |                114.3% |
|     Calhoun |                    2.1 |                            22.2 |                119.9% |
|       Emmet |                    2.0 |                            21.7 |               \-36.4% |
|       Scott |                   37.0 |                            21.4 |               \-20.8% |
| Cerro Gordo |                    9.0 |                            21.2 |                  6.1% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|    Union |                    4.7 |                            38.5 |              3 895.8% |
|  Calhoun |                    2.1 |                            22.2 |                119.9% |
| Ringgold |                    1.1 |                            23.4 |                114.3% |
|    Wayne |                    1.1 |                            17.7 |                 87.5% |
| Franklin |                    2.7 |                            27.0 |                 44.5% |
|    Davis |                    0.9 |                             9.5 |                 44.4% |
| Marshall |                    2.9 |                             7.3 |                 35.0% |
|    Adair |                    1.4 |                            20.0 |                 30.8% |
|    Adams |                    0.9 |                            23.8 |                 30.0% |
|   Howard |                    1.1 |                            12.5 |                 25.0% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Osceola |                    0.3 |                             4.8 |               \-70.0% |
|  Plymouth |                    0.6 |                             2.3 |               \-62.1% |
|   Jackson |                    0.7 |                             3.7 |               \-53.9% |
|      Clay |                    1.6 |                             9.8 |               \-51.4% |
|     Sioux |                    1.9 |                             5.3 |               \-51.2% |
| Jefferson |                    0.3 |                             1.6 |               \-50.0% |
|   Kossuth |                    0.6 |                             3.9 |               \-50.0% |
|       Sac |                    0.9 |                             8.8 |               \-50.0% |
| Palo Alto |                    0.3 |                             3.2 |               \-47.1% |
|  Woodbury |                    8.4 |                             8.2 |               \-46.8% |
