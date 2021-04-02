Compiled at 2021-04-02 20:24:19 UTC

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

## Tables as of 2021-04-02

As of 2021-04-02, IPDH is reporting 611 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |
| 2021-04-01 |                  654.4 |                            20.7 |                 23.0% |
| 2021-03-31 |                  648.1 |                            20.5 |                 53.4% |
| 2021-03-30 |                  560.1 |                            17.8 |                 36.0% |
| 2021-03-28 |                  579.9 |                            18.4 |                 38.3% |
| 2021-03-27 |                  540.1 |                            17.1 |                 30.4% |
| 2021-03-26 |                  528.3 |                            16.7 |                 23.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  126.3 |                            25.8 |                 29.3% |
|          Linn |                   21.4 |                             9.5 |                 18.9% |
|         Scott |                   73.6 |                            42.5 |                 91.9% |
|       Johnson |                   26.6 |                            17.6 |                 45.1% |
|    Black Hawk |                   16.6 |                            12.6 |                 33.7% |
|      Woodbury |                   30.9 |                            29.9 |                  4.7% |
|       Dubuque |                   22.4 |                            23.0 |                 60.8% |
|         Story |                   27.6 |                            28.4 |                 68.1% |
|        Dallas |                   25.0 |                            26.8 |                 43.3% |
| Pottawattamie |                   27.1 |                            29.1 |                 27.1% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
| Dickinson |                   13.6 |                            78.6 |                 30.8% |
|      Clay |                    9.6 |                            59.8 |                 23.3% |
|     Emmet |                    5.3 |                            57.4 |                 37.5% |
| Palo Alto |                    4.3 |                            48.2 |                 85.0% |
|   Osceola |                    2.6 |                            43.2 |                 19.0% |
|     Scott |                   73.6 |                            42.5 |                 91.9% |
|  Delaware |                    6.9 |                            40.3 |                 71.9% |
|  Plymouth |                   10.0 |                            39.7 |                 42.6% |
|   Guthrie |                    4.0 |                            37.4 |                 20.7% |
|       Lee |                   12.3 |                            36.5 |                675.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Lee |                   12.3 |                            36.5 |                675.1% |
|     Cedar |                    5.0 |                            26.8 |                162.5% |
|    Clarke |                    1.6 |                            16.7 |                124.9% |
|   Clinton |                   13.1 |                            28.3 |                 94.1% |
|     Scott |                   73.6 |                            42.5 |                 91.9% |
| Palo Alto |                    4.3 |                            48.2 |                 85.0% |
|  Mitchell |                    2.1 |                            20.2 |                 83.4% |
|     Henry |                    2.7 |                            13.6 |                 73.3% |
|  Delaware |                    6.9 |                            40.3 |                 71.9% |
|     Story |                   27.6 |                            28.4 |                 68.1% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Wapello |                    3.6 |                            10.2 |               \-47.5% |
|     Tama |                    0.4 |                             2.5 |               \-44.4% |
|    Wayne |                    0.9 |                            13.3 |               \-38.1% |
| Harrison |                    1.0 |                             7.1 |               \-33.3% |
|    Lucas |                    0.1 |                             1.7 |               \-33.3% |
| Humboldt |                    1.3 |                            13.5 |               \-30.4% |
|  Calhoun |                    0.7 |                             7.4 |               \-29.4% |
|   Butler |                    0.6 |                             4.0 |               \-26.7% |
|     Iowa |                    0.7 |                             4.4 |               \-25.0% |
|      Ida |                    1.1 |                            16.7 |               \-25.0% |
