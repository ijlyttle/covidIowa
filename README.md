Compiled at 2021-04-09 20:23:06 UTC

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

## Tables as of 2021-04-09

As of 2021-04-09, IPDH is reporting 519 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-09 |                  512.0 |                            16.2 |               \-21.4% |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   85.0 |                            17.3 |               \-32.4% |
|          Linn |                   21.0 |                             9.3 |                \-1.9% |
|         Scott |                   56.3 |                            32.5 |               \-23.2% |
|       Johnson |                   28.7 |                            19.0 |                  7.8% |
|    Black Hawk |                   16.7 |                            12.7 |                  0.8% |
|      Woodbury |                   21.3 |                            20.6 |               \-30.0% |
|       Dubuque |                   28.0 |                            28.8 |                 23.8% |
|         Story |                   15.4 |                            15.9 |               \-42.5% |
|        Dallas |                   12.3 |                            13.1 |               \-48.9% |
| Pottawattamie |                   26.3 |                            28.2 |                \-3.0% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   10.9 |                            62.9 |               \-18.6% |
|     Emmet |                    4.0 |                            43.4 |               \-20.5% |
|      Clay |                    5.9 |                            36.6 |               \-35.1% |
|  Plymouth |                    8.4 |                            33.5 |               \-14.3% |
|     Scott |                   56.3 |                            32.5 |               \-23.2% |
|  Delaware |                    5.1 |                            30.2 |               \-21.8% |
|  Harrison |                    4.1 |                            29.5 |                157.1% |
|   Kossuth |                    4.3 |                            28.9 |                  5.7% |
|   Dubuque |                   28.0 |                            28.8 |                 23.8% |
|   Osceola |                    1.7 |                            28.8 |               \-24.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Harrison |                    4.1 |                            29.5 |                157.1% |
|    Carroll |                    5.4 |                            26.9 |                104.5% |
|    Clayton |                    3.1 |                            17.9 |                 81.2% |
|     Taylor |                    0.7 |                            11.7 |                 71.4% |
|     Monroe |                    1.4 |                            18.5 |                 54.6% |
|      Worth |                    1.7 |                            23.2 |                 46.1% |
|    Mahaska |                    3.0 |                            13.6 |                 40.0% |
|       Tama |                    1.0 |                             5.9 |                 40.0% |
|      Davis |                    1.6 |                            17.5 |                 38.4% |
| Washington |                    3.4 |                            15.6 |                 34.8% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                    2.9 |                             8.5 |               \-71.0% |
|    Guthrie |                    0.7 |                             6.7 |               \-65.7% |
|     Clarke |                    0.1 |                             1.5 |               \-55.5% |
|     Jasper |                    2.9 |                             7.7 |               \-54.2% |
|   Mitchell |                    0.6 |                             5.4 |               \-50.0% |
| Pocahontas |                    0.0 |                             0.0 |               \-50.0% |
|     Dallas |                   12.3 |                            13.1 |               \-48.9% |
|     Benton |                    1.1 |                             4.5 |               \-46.4% |
|   Humboldt |                    0.3 |                             3.0 |               \-43.7% |
|      Story |                   15.4 |                            15.9 |               \-42.5% |
