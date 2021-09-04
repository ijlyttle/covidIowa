Compiled at 2021-09-04 17:21:54 UTC

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

## Tables as of 2021-09-02

As of 2021-09-02, IPDH is reporting -1.768110^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  128.9 |                            26.3 |                410.7% |
|          Linn |                   51.3 |                            22.6 |                590.6% |
|         Scott |                   40.3 |                            23.3 |                389.8% |
|       Johnson |                   25.1 |                            16.6 |                245.3% |
|    Black Hawk |                   64.6 |                            49.2 |                206.0% |
|      Woodbury |                   31.7 |                            30.8 |                340.4% |
|       Dubuque |                   11.6 |                            11.9 |                300.0% |
|         Story |                   28.6 |                            29.4 |                305.9% |
|        Dallas |                   26.3 |                            28.1 |                289.8% |
| Pottawattamie |                   28.3 |                            30.3 |                388.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   35.7 |                           106.1 |                851.9% |
|    Webster |                   28.1 |                            78.4 |                112.5% |
|        Ida |                    5.0 |                            72.9 |                319.9% |
| Des Moines |                   26.0 |                            66.7 |                361.0% |
|      Davis |                    5.3 |                            58.7 |                450.0% |
|   Franklin |                    5.7 |                            56.7 |                147.4% |
|   Crawford |                    9.4 |                            56.1 |                421.4% |
|     Wright |                    6.7 |                            53.4 |                116.0% |
|   Humboldt |                    5.0 |                            52.3 |                 90.9% |
|    Kossuth |                    7.4 |                            50.2 |                195.0% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|           Lee |                   35.7 |                           106.1 |                851.9% |
|          Linn |                   51.3 |                            22.6 |                590.6% |
|         Davis |                    5.3 |                            58.7 |                450.0% |
|      Marshall |                    7.6 |                            19.2 |                445.6% |
|      Crawford |                    9.4 |                            56.1 |                421.4% |
|          Polk |                  128.9 |                            26.3 |                410.7% |
|         Scott |                   40.3 |                            23.3 |                389.8% |
|     Muscatine |                   11.6 |                            27.1 |                389.0% |
|     Jefferson |                    5.3 |                            28.9 |                388.8% |
| Pottawattamie |                   28.3 |                            30.3 |                388.1% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Montgomery |                    0.7 |                             7.2 |               \-29.4% |
|   Mitchell |                    0.1 |                             1.4 |                  0.0% |
|     Taylor |                    0.1 |                             2.3 |                  0.0% |
|      Adair |                    1.9 |                            26.0 |                 17.6% |
|    Decatur |                    2.0 |                            25.4 |                 31.2% |
| Winneshiek |                    1.3 |                             6.4 |                 33.4% |
|     Monroe |                    3.4 |                            44.5 |                 34.8% |
|    Fremont |                    0.7 |                            10.3 |                 50.0% |
|      Adams |                    1.6 |                            43.6 |                 50.0% |
|    Calhoun |                    4.3 |                            44.3 |                 54.2% |
