Compiled at 2021-04-21 17:12:21 UTC

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

## Tables as of 2021-04-21

As of 2021-04-21, IPDH is reporting 631 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |
| 2021-04-15 |                  478.7 |                            15.2 |                \-8.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   80.3 |                            16.4 |                \-9.2% |
|          Linn |                   26.6 |                            11.7 |                 10.3% |
|         Scott |                   54.7 |                            31.6 |                \-3.5% |
|       Johnson |                   30.6 |                            20.2 |                  3.3% |
|    Black Hawk |                   16.3 |                            12.4 |                  3.4% |
|      Woodbury |                   15.9 |                            15.4 |               \-26.7% |
|       Dubuque |                   14.9 |                            15.3 |               \-36.6% |
|         Story |                   11.9 |                            12.2 |                \-3.2% |
|        Dallas |                   12.0 |                            12.8 |                \-6.2% |
| Pottawattamie |                   20.4 |                            21.9 |               \-12.8% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Osceola |                    3.4 |                            57.6 |                 10.7% |
|         Scott |                   54.7 |                            31.6 |                \-3.5% |
|        Shelby |                    3.3 |                            28.7 |                 20.0% |
|     Dickinson |                    4.9 |                            28.1 |               \-29.3% |
|         Emmet |                    2.6 |                            27.9 |               \-16.7% |
|          Clay |                    4.3 |                            26.8 |                  5.7% |
|           Sac |                    2.6 |                            26.4 |                 47.0% |
|     Palo Alto |                    2.1 |                            24.1 |                 29.4% |
|     Muscatine |                    9.4 |                            22.1 |                \-2.7% |
| Pottawattamie |                   20.4 |                            21.9 |               \-12.8% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Monona |                    1.4 |                            16.6 |                112.5% |
|  Jefferson |                    0.9 |                             4.7 |                 85.7% |
|  Winnebago |                    2.1 |                            20.7 |                 69.3% |
|      Lucas |                    1.1 |                            13.3 |                 66.6% |
|    Fayette |                    1.0 |                             5.1 |                 55.5% |
| Pocahontas |                    1.0 |                            15.1 |                 55.5% |
|     Benton |                    2.4 |                             9.5 |                 50.0% |
|        Sac |                    2.6 |                            26.4 |                 47.0% |
|     Howard |                    0.6 |                             6.2 |                 37.4% |
|   Crawford |                    1.7 |                            10.2 |                 35.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
|       Page |                    0.7 |                             4.7 |               \-57.2% |
|    Fremont |                    0.6 |                             8.2 |               \-52.2% |
| Washington |                    1.0 |                             4.6 |               \-48.1% |
|    Wapello |                    0.9 |                             2.5 |               \-48.0% |
|    Clayton |                    1.4 |                             8.1 |               \-43.3% |
|      Davis |                    0.0 |                             0.0 |               \-41.7% |
|      Mills |                    1.3 |                             8.5 |               \-40.7% |
|   Harrison |                    1.9 |                            13.2 |               \-39.4% |
|  Appanoose |                    0.1 |                             1.2 |               \-38.4% |
