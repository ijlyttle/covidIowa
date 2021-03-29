Compiled at 2021-03-29 17:17:15 UTC

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

## Tables as of 2021-03-28

As of 2021-03-28, IPDH is reporting 595 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  118.0 |                            24.1 |                 23.0% |
|          Linn |                   16.3 |                             7.2 |                  3.4% |
|         Scott |                   58.4 |                            33.8 |                136.4% |
|       Johnson |                   22.6 |                            14.9 |                 75.5% |
|    Black Hawk |                   14.9 |                            11.3 |                 46.1% |
|      Woodbury |                   28.9 |                            28.0 |                  1.5% |
|       Dubuque |                   17.3 |                            17.8 |                113.3% |
|         Story |                   20.1 |                            20.7 |                 48.0% |
|        Dallas |                   23.6 |                            25.2 |                 60.7% |
| Pottawattamie |                   22.1 |                            23.8 |                 35.0% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.7 |                            67.9 |                 20.3% |
|     Emmet |                    5.3 |                            57.4 |                 76.0% |
|      Clay |                    9.1 |                            57.1 |                 61.4% |
|   Osceola |                    3.0 |                            50.4 |                133.4% |
|   Guthrie |                    3.9 |                            36.1 |                142.9% |
|    Shelby |                    4.0 |                            34.9 |                105.8% |
|       Lee |                   11.4 |                            34.0 |                769.8% |
|     Scott |                   58.4 |                            33.8 |                136.4% |
|   O’Brien |                    4.4 |                            32.2 |                  2.7% |
| Palo Alto |                    2.9 |                            32.2 |                 42.1% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   11.4 |                            34.0 |                769.8% |
|     Jasper |                   11.4 |                            30.7 |                210.7% |
|    Guthrie |                    3.9 |                            36.1 |                142.9% |
|      Scott |                   58.4 |                            33.8 |                136.4% |
|    Osceola |                    3.0 |                            50.4 |                133.4% |
|    Dubuque |                   17.3 |                            17.8 |                113.3% |
|     Shelby |                    4.0 |                            34.9 |                105.8% |
| Washington |                    3.3 |                            15.0 |                 87.5% |
|      Emmet |                    5.3 |                            57.4 |                 76.0% |
|    Johnson |                   22.6 |                            14.9 |                 75.5% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Crawford |                    0.9 |                             5.1 |               \-48.0% |
|    Wapello |                    4.0 |                            11.4 |               \-47.8% |
|      Adair |                    0.3 |                             4.0 |               \-47.1% |
|  Poweshiek |                    0.4 |                             2.3 |               \-44.4% |
|     Monroe |                    0.1 |                             1.9 |               \-42.8% |
|  Chickasaw |                    0.1 |                             1.2 |               \-38.4% |
|      Lucas |                    0.4 |                             5.0 |               \-37.5% |
|    Calhoun |                    0.7 |                             7.4 |               \-36.8% |
|  Appanoose |                    0.6 |                             4.6 |               \-31.3% |
| Pocahontas |                    0.6 |                             8.6 |               \-26.7% |
