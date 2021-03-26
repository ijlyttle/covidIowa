Compiled at 2021-03-26 17:12:45 UTC

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

## Tables as of 2021-03-26

As of 2021-03-26, IPDH is reporting 907 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |
| 2021-03-20 |                  414.0 |                            13.1 |               \-10.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  103.7 |                            21.2 |                  7.5% |
|          Linn |                   16.3 |                             7.2 |                  0.0% |
|         Scott |                   52.3 |                            30.2 |                127.4% |
|       Johnson |                   21.1 |                            14.0 |                 91.4% |
|    Black Hawk |                   11.9 |                             9.0 |                \-2.2% |
|      Woodbury |                   26.1 |                            25.4 |               \-19.1% |
|       Dubuque |                   14.7 |                            15.1 |                 74.6% |
|         Story |                   18.4 |                            19.0 |                 46.2% |
|        Dallas |                   19.4 |                            20.8 |                 30.0% |
| Pottawattamie |                   20.9 |                            22.4 |                 40.4% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.3 |                            65.4 |                 34.4% |
|      Clay |                    9.7 |                            60.7 |                 78.6% |
|     Emmet |                    3.9 |                            41.9 |                 21.4% |
|   Osceola |                    2.4 |                            40.8 |                118.3% |
|       Lee |                   11.3 |                            33.5 |                759.8% |
|    Shelby |                    3.7 |                            32.4 |                 73.7% |
|   Kossuth |                    4.7 |                            31.8 |                 14.3% |
|     Scott |                   52.3 |                            30.2 |                127.4% |
|  Plymouth |                    7.3 |                            28.9 |                 16.0% |
|   Fremont |                    2.0 |                            28.7 |                 61.6% |

Most growth in positive cases, week-over-week:

|  county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------: | ---------------------: | ------------------------------: | --------------------: |
|     Lee |                   11.3 |                            33.5 |                759.8% |
|  Jasper |                   10.3 |                            27.7 |                243.5% |
|   Scott |                   52.3 |                            30.2 |                127.4% |
| Osceola |                    2.4 |                            40.8 |                118.3% |
| Johnson |                   21.1 |                            14.0 |                 91.4% |
| Guthrie |                    3.0 |                            28.1 |                 86.7% |
| Jackson |                    2.9 |                            14.7 |                 80.0% |
|    Clay |                    9.7 |                            60.7 |                 78.6% |
| Dubuque |                   14.7 |                            15.1 |                 74.6% |
|  Shelby |                    3.7 |                            32.4 |                 73.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|  Poweshiek |                    0.4 |                             2.3 |               \-52.4% |
|      Adair |                    0.3 |                             4.0 |               \-47.1% |
|      Lucas |                    0.4 |                             5.0 |               \-44.4% |
|     Monroe |                    0.1 |                             1.9 |               \-42.8% |
|  Chickasaw |                    0.1 |                             1.2 |               \-38.4% |
| Pocahontas |                    0.6 |                             8.6 |               \-35.3% |
|      Jones |                    1.3 |                             6.2 |               \-33.3% |
|   Crawford |                    1.4 |                             8.5 |               \-32.0% |
|    Calhoun |                    0.9 |                             8.9 |               \-31.6% |
|   Hamilton |                    0.7 |                             4.8 |               \-29.4% |
