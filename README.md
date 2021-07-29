Compiled at 2021-07-29 17:26:06 UTC

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

## Tables as of 2021-07-28

As of 2021-07-28, IPDH is reporting 2157 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   68.4 |                            14.0 |                262.7% |
|          Linn |                   23.7 |                            10.5 |                246.0% |
|         Scott |                   21.0 |                            12.1 |                214.3% |
|       Johnson |                   15.3 |                            10.1 |                418.2% |
|    Black Hawk |                   42.4 |                            32.3 |                153.3% |
|      Woodbury |                   14.9 |                            14.4 |                164.3% |
|       Dubuque |                    7.1 |                             7.3 |                185.0% |
|         Story |                   19.7 |                            20.3 |                625.0% |
|        Dallas |                   15.9 |                            17.0 |                293.3% |
| Pottawattamie |                   17.0 |                            18.2 |                320.0% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Webster |                   21.9 |                            60.9 |                107.8% |
|   Monroe |                    4.0 |                            51.9 |                133.3% |
| Humboldt |                    4.4 |                            46.3 |                171.5% |
| Hamilton |                    6.7 |                            45.4 |                157.1% |
|  Kossuth |                    6.6 |                            44.4 |                307.7% |
|  Calhoun |                    3.7 |                            38.4 |                 43.5% |
|    Davis |                    3.4 |                            38.1 |                287.5% |
|   Wright |                    4.6 |                            36.4 |                 69.5% |
|      Lee |                   12.0 |                            35.7 |                250.0% |
| Franklin |                    3.3 |                            32.6 |                 50.0% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|         Story |                   19.7 |                            20.3 |                625.0% |
|       Johnson |                   15.3 |                            10.1 |                418.2% |
|     Muscatine |                    7.1 |                            16.7 |                375.1% |
|      Crawford |                    5.1 |                            30.6 |                329.9% |
| Pottawattamie |                   17.0 |                            18.2 |                320.0% |
|       Kossuth |                    6.6 |                            44.4 |                307.7% |
|        Dallas |                   15.9 |                            17.0 |                293.3% |
|         Davis |                    3.4 |                            38.1 |                287.5% |
|          Polk |                   68.4 |                            14.0 |                262.7% |
|           Lee |                   12.0 |                            35.7 |                250.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Mitchell |                    0.1 |                             1.4 |               \-42.8% |
|     Keokuk |                    0.9 |                             8.4 |               \-23.5% |
|      Union |                    0.0 |                             0.0 |               \-22.2% |
|    Madison |                    1.1 |                             7.0 |               \-16.6% |
| Montgomery |                    1.1 |                            11.5 |               \-11.8% |
|    Fremont |                    0.1 |                             2.1 |               \-11.1% |
|      Adams |                    0.6 |                            15.9 |                \-8.3% |
|     Shelby |                    1.0 |                             8.7 |                \-6.7% |
|    Decatur |                    1.6 |                            20.0 |                  5.8% |
| Pocahontas |                    0.4 |                             6.5 |                 11.1% |
