Compiled at 2021-05-03 00:01:10 UTC

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

## Tables as of 2021-05-02

As of 2021-05-02, IPDH is reporting 326 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |
| 2021-04-30 |                  362.0 |                            11.5 |               \-15.0% |
| 2021-04-29 |                  370.4 |                            11.7 |               \-17.2% |
| 2021-04-28 |                  373.6 |                            11.8 |               \-17.6% |
| 2021-04-27 |                  391.9 |                            12.4 |               \-14.2% |
| 2021-04-26 |                  420.9 |                            13.3 |                \-4.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   64.9 |                            13.2 |               \-17.5% |
|          Linn |                   22.1 |                             9.8 |               \-14.3% |
|         Scott |                   38.1 |                            22.1 |                \-0.4% |
|       Johnson |                   20.3 |                            13.4 |               \-17.7% |
|    Black Hawk |                   11.3 |                             8.6 |                \-7.5% |
|      Woodbury |                    8.1 |                             7.9 |               \-39.0% |
|       Dubuque |                    8.7 |                             9.0 |               \-12.8% |
|         Story |                   15.1 |                            15.6 |                 15.3% |
|        Dallas |                   10.0 |                            10.7 |               \-27.4% |
| Pottawattamie |                   15.7 |                            16.9 |               \-18.7% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    5.4 |                            44.4 |              4 395.8% |
| Winnebago |                    2.9 |                            27.6 |               \-10.0% |
|     Worth |                    1.9 |                            25.2 |                  5.3% |
|  Franklin |                    2.4 |                            24.1 |                 20.0% |
|     Adams |                    0.9 |                            23.8 |                 30.0% |
|  Ringgold |                    1.1 |                            23.4 |                114.3% |
|     Scott |                   38.1 |                            22.1 |                \-0.4% |
|     Emmet |                    2.0 |                            21.7 |               \-34.4% |
|   Hancock |                    2.3 |                            21.5 |                 53.3% |
|   Madison |                    3.4 |                            21.0 |                 10.7% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|    Union |                    5.4 |                            44.4 |              4 395.8% |
| Ringgold |                    1.1 |                            23.4 |                114.3% |
|  Calhoun |                    2.0 |                            20.7 |                 91.0% |
|    Wayne |                    1.1 |                            17.7 |                 87.5% |
|  Hancock |                    2.3 |                            21.5 |                 53.3% |
|  Wapello |                    1.6 |                             4.5 |                 50.0% |
| Marshall |                    3.0 |                             7.6 |                 40.0% |
|   Butler |                    1.0 |                             6.9 |                 40.0% |
|    Mills |                    2.1 |                            14.2 |                 37.5% |
|   Grundy |                    0.6 |                             4.7 |                 37.4% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|  Osceola |                    0.3 |                             4.8 |               \-65.4% |
|      Sac |                    0.7 |                             7.3 |               \-50.0% |
| Plymouth |                    0.9 |                             3.4 |               \-48.0% |
|  Jackson |                    0.9 |                             4.4 |               \-43.5% |
|  Kossuth |                    0.7 |                             4.8 |               \-42.9% |
|    Sioux |                    1.7 |                             4.9 |               \-42.4% |
| Woodbury |                    8.1 |                             7.9 |               \-39.0% |
|     Clay |                    1.6 |                             9.8 |               \-35.7% |
|    Floyd |                    1.9 |                            11.9 |               \-35.5% |
|  O’Brien |                    0.9 |                             6.2 |               \-35.0% |
