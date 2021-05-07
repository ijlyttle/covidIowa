Compiled at 2021-05-07 20:18:10 UTC

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

## Tables as of 2021-05-07

As of 2021-05-07, IPDH is reporting 398 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-07 |                  352.0 |                            11.2 |                \-2.8% |
| 2021-05-06 |                  348.3 |                            11.0 |                \-6.0% |
| 2021-05-05 |                  314.6 |                            10.0 |               \-15.8% |
| 2021-05-04 |                  366.7 |                            11.6 |                \-6.4% |
| 2021-05-03 |                  362.9 |                            11.5 |               \-13.7% |
| 2021-05-02 |                  370.3 |                            11.7 |               \-11.6% |
| 2021-05-01 |                  355.1 |                            11.3 |               \-27.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   64.0 |                            13.1 |                  2.9% |
|          Linn |                   21.1 |                             9.3 |                \-8.8% |
|         Scott |                   38.6 |                            22.3 |                  3.4% |
|       Johnson |                   12.1 |                             8.0 |               \-34.8% |
|    Black Hawk |                    9.1 |                             7.0 |                \-6.6% |
|      Woodbury |                    8.0 |                             7.8 |                \-1.6% |
|       Dubuque |                    7.9 |                             8.1 |                  0.0% |
|         Story |                   11.9 |                            12.2 |               \-15.1% |
|        Dallas |                   10.9 |                            11.6 |                \-3.5% |
| Pottawattamie |                   14.7 |                            15.8 |                \-1.8% |

Most positive-cases, per-capita:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Ringgold |                    2.1 |                            43.8 |                100.1% |
|   Madison |                    5.3 |                            32.4 |                120.0% |
|  Franklin |                    3.1 |                            31.2 |                 16.0% |
|   Calhoun |                    2.9 |                            29.6 |                 35.0% |
|     Union |                    3.3 |                            26.8 |                \-3.2% |
|     Emmet |                    2.3 |                            24.8 |                \-8.0% |
|     Scott |                   38.6 |                            22.3 |                  3.4% |
|   Audubon |                    1.1 |                            20.8 |                 50.0% |
|     Davis |                    1.9 |                            20.6 |                 53.9% |
| Muscatine |                    8.4 |                            19.8 |                 26.9% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Crawford |                    3.1 |                            18.7 |                163.7% |
|   Madison |                    5.3 |                            32.4 |                120.0% |
|     Boone |                    3.1 |                            12.0 |                107.1% |
|  Ringgold |                    2.1 |                            43.8 |                100.1% |
| Chickasaw |                    1.3 |                            10.8 |                100.0% |
|   Wapello |                    3.0 |                             8.6 |                 75.0% |
|     Sioux |                    4.0 |                            11.5 |                 75.0% |
|    Butler |                    1.7 |                            11.9 |                 72.8% |
|  Plymouth |                    1.4 |                             5.7 |                 70.0% |
|    Shelby |                    1.4 |                            12.5 |                 70.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                    0.3 |                             1.5 |               \-52.6% |
|       Adair |                    0.3 |                             4.0 |               \-50.0% |
|      Howard |                    0.3 |                             3.1 |               \-47.1% |
|        Clay |                    0.7 |                             4.5 |               \-45.5% |
|    Delaware |                    1.3 |                             7.6 |               \-44.8% |
|     Hancock |                    1.0 |                             9.4 |               \-44.0% |
|       Worth |                    0.9 |                            11.6 |               \-43.5% |
|   Dickinson |                    1.3 |                             7.5 |               \-42.8% |
|         Ida |                  \-0.1 |                           \-2.1 |               \-40.0% |
|  Pocahontas |                    0.3 |                             4.3 |               \-40.0% |
