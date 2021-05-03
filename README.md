Compiled at 2021-05-03 20:18:05 UTC

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

## Tables as of 2021-05-03

As of 2021-05-03, IPDH is reporting 130 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   62.7 |                            12.8 |               \-22.7% |
|          Linn |                   22.4 |                             9.9 |                \-7.9% |
|         Scott |                   39.3 |                            22.7 |                  4.4% |
|       Johnson |                   18.7 |                            12.4 |               \-24.2% |
|    Black Hawk |                   11.1 |                             8.5 |                \-9.6% |
|      Woodbury |                    8.1 |                             7.9 |               \-39.6% |
|       Dubuque |                    8.3 |                             8.5 |               \-16.7% |
|         Story |                   14.9 |                            15.3 |                  8.8% |
|        Dallas |                   10.3 |                            11.0 |               \-28.2% |
| Pottawattamie |                   15.6 |                            16.7 |               \-14.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.4 |                            44.4 |              4 395.8% |
| Winnebago |                    2.7 |                            26.2 |               \-16.1% |
|     Worth |                    1.9 |                            25.2 |                 11.1% |
|  Franklin |                    2.4 |                            24.1 |                 20.0% |
|     Adams |                    0.9 |                            23.8 |                 30.0% |
|   Madison |                    3.9 |                            23.6 |                 30.8% |
|  Ringgold |                    1.1 |                            23.4 |                114.3% |
|     Emmet |                    2.1 |                            23.3 |               \-29.0% |
|     Scott |                   39.3 |                            22.7 |                  4.4% |
|   Calhoun |                    2.1 |                            22.2 |                119.9% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.4 |                            44.4 |              4 395.8% |
|   Calhoun |                    2.1 |                            22.2 |                119.9% |
|  Ringgold |                    1.1 |                            23.4 |                114.3% |
|     Wayne |                    1.3 |                            20.0 |                100.0% |
|    Grundy |                    0.7 |                             5.8 |                 50.0% |
|   Hancock |                    2.1 |                            20.2 |                 46.7% |
|   Wapello |                    1.7 |                             4.9 |                 46.1% |
|    Butler |                    1.0 |                             6.9 |                 40.0% |
| Appanoose |                    1.1 |                             9.2 |                 36.4% |
|  Crawford |                    1.7 |                            10.2 |                 35.7% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Osceola |                    0.3 |                             4.8 |               \-62.5% |
| Plymouth |                    0.7 |                             2.8 |               \-47.8% |
|      Sac |                    0.7 |                             7.3 |               \-47.8% |
|  Kossuth |                    0.6 |                             3.9 |               \-42.1% |
| Woodbury |                    8.1 |                             7.9 |               \-39.6% |
|    Floyd |                    1.9 |                            11.9 |               \-39.4% |
|     Clay |                    1.4 |                             8.9 |               \-39.3% |
|  O’Brien |                    0.9 |                             6.2 |               \-38.1% |
|   Warren |                    7.9 |                            15.3 |               \-33.3% |
|  Carroll |                    2.4 |                            12.0 |               \-33.3% |
