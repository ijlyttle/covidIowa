Compiled at 2021-09-11 20:15:06 UTC

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

## Tables as of 2021-09-08

As of 2021-09-08, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-08 |                  818.1 |                            25.9 |                308.7% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  122.7 |                            25.0 |                348.7% |
|          Linn |                   50.0 |                            22.1 |                485.3% |
|         Scott |                   38.9 |                            22.5 |                381.0% |
|       Johnson |                   23.9 |                            15.8 |                200.0% |
|    Black Hawk |                   62.0 |                            47.2 |                192.1% |
|      Woodbury |                   29.9 |                            29.0 |                266.1% |
|       Dubuque |                   10.9 |                            11.2 |                219.3% |
|         Story |                   27.6 |                            28.4 |                292.1% |
|        Dallas |                   24.9 |                            26.6 |                229.1% |
| Pottawattamie |                   27.6 |                            29.6 |                365.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   31.7 |                            94.2 |                324.1% |
|        Ida |                    4.9 |                            70.8 |                309.9% |
|    Webster |                   25.0 |                            69.6 |                 93.6% |
| Des Moines |                   23.4 |                            60.1 |                297.7% |
|   Crawford |                    9.3 |                            55.2 |                414.3% |
|     Wright |                    6.4 |                            51.2 |                126.1% |
|   Franklin |                    5.1 |                            51.1 |                104.8% |
|      Davis |                    4.3 |                            47.6 |                146.7% |
|     Marion |                   15.7 |                            47.3 |                317.9% |
| Black Hawk |                   62.0 |                            47.2 |                192.1% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|      Marshall |                    7.6 |                            19.2 |                566.5% |
|          Linn |                   50.0 |                            22.1 |                485.3% |
|     Jefferson |                    5.3 |                            28.9 |                450.0% |
|      Crawford |                    9.3 |                            55.2 |                414.3% |
|         Scott |                   38.9 |                            22.5 |                381.0% |
|       Wapello |                    9.9 |                            28.2 |                374.9% |
|        Jasper |                   11.9 |                            31.9 |                373.7% |
| Pottawattamie |                   27.6 |                            29.6 |                365.1% |
|    Washington |                    4.9 |                            22.1 |                355.4% |
|          Polk |                  122.7 |                            25.0 |                348.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Montgomery |                    0.6 |                             5.8 |               \-31.3% |
|     Taylor |                    0.0 |                             0.0 |               \-22.2% |
|     Monroe |                    2.4 |                            31.5 |               \-17.2% |
|    Decatur |                    1.4 |                            18.2 |               \-10.5% |
|   Mitchell |                    0.1 |                             1.4 |                  0.0% |
|      Adair |                    1.6 |                            22.0 |                  0.0% |
|   Ringgold |                    1.0 |                            20.4 |                 27.3% |
| Winneshiek |                    1.3 |                             6.4 |                 33.4% |
|    Jackson |                    0.9 |                             4.4 |                 44.4% |
|    Clayton |                    2.1 |                            12.2 |                 46.7% |
