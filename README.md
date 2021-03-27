Compiled at 2021-03-27 20:20:36 UTC

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

## Tables as of 2021-03-27

As of 2021-03-27, IPDH is reporting 531 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |
| 2021-03-25 |                  483.7 |                            15.3 |                 16.9% |
| 2021-03-24 |                  531.7 |                            16.9 |                 59.0% |
| 2021-03-23 |                  422.3 |                            13.4 |                \-5.8% |
| 2021-03-22 |                  411.6 |                            13.0 |               \-11.1% |
| 2021-03-21 |                  419.0 |                            13.3 |               \-17.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  106.4 |                            21.7 |                 12.2% |
|          Linn |                   16.3 |                             7.2 |                  7.1% |
|         Scott |                   55.9 |                            32.3 |                135.5% |
|       Johnson |                   21.6 |                            14.3 |                 95.1% |
|    Black Hawk |                   12.4 |                             9.5 |                 20.5% |
|      Woodbury |                   24.3 |                            23.6 |               \-16.9% |
|       Dubuque |                   16.0 |                            16.4 |                101.7% |
|         Story |                   19.3 |                            19.9 |                 46.4% |
|        Dallas |                   19.4 |                            20.8 |                 32.4% |
| Pottawattamie |                   20.9 |                            22.4 |                 25.4% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   11.4 |                            66.2 |                 24.3% |
|      Clay |                    9.1 |                            57.1 |                 82.1% |
|     Emmet |                    4.6 |                            49.6 |                 50.0% |
|   Osceola |                    2.7 |                            45.6 |                116.7% |
|    Shelby |                    4.0 |                            34.9 |                118.7% |
|       Lee |                   11.4 |                            34.0 |                769.8% |
|     Scott |                   55.9 |                            32.3 |                135.5% |
|   O’Brien |                    4.4 |                            32.2 |                  0.0% |
|   Guthrie |                    3.4 |                            32.1 |                121.4% |
|   Kossuth |                    4.6 |                            30.9 |                  0.0% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Lee |                   11.4 |                            34.0 |                769.8% |
|   Jasper |                   10.0 |                            26.9 |                185.2% |
|    Scott |                   55.9 |                            32.3 |                135.5% |
|  Guthrie |                    3.4 |                            32.1 |                121.4% |
|   Shelby |                    4.0 |                            34.9 |                118.7% |
|  Osceola |                    2.7 |                            45.6 |                116.7% |
|  Dubuque |                   16.0 |                            16.4 |                101.7% |
|  Johnson |                   21.6 |                            14.3 |                 95.1% |
|     Clay |                    9.1 |                            57.1 |                 82.1% |
| Delaware |                    5.1 |                            30.2 |                 72.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|  Poweshiek |                    0.3 |                             1.5 |               \-50.0% |
|      Adair |                    0.3 |                             4.0 |               \-47.1% |
|    Wapello |                    4.1 |                            11.8 |               \-44.6% |
|     Monroe |                    0.1 |                             1.9 |               \-42.8% |
|    Clayton |                    0.6 |                             3.3 |               \-38.9% |
|      Lucas |                    0.4 |                             5.0 |               \-37.5% |
| Pocahontas |                    0.4 |                             6.5 |               \-37.5% |
|  Appanoose |                    0.6 |                             4.6 |               \-35.3% |
|    Calhoun |                    0.9 |                             8.9 |               \-31.6% |
|       Iowa |                    1.0 |                             6.2 |               \-30.0% |
