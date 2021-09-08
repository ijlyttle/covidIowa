Compiled at 2021-09-08 20:17:27 UTC

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

As of 2021-09-08, IPDH is reporting 3.439310^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-08 |                 5731.4 |                           181.7 |              2 760.1% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  935.0 |                           190.8 |              3 294.9% |
|          Linn |                  470.3 |                           207.4 |              5 308.4% |
|         Scott |                  283.1 |                           163.7 |              3 329.2% |
|       Johnson |                  208.6 |                           138.0 |              2 429.2% |
|    Black Hawk |                  302.0 |                           230.1 |              1 304.7% |
|      Woodbury |                  163.1 |                           158.2 |              1 847.4% |
|       Dubuque |                  101.6 |                           104.4 |              2 661.7% |
|         Story |                  118.1 |                           121.7 |              1 535.2% |
|        Dallas |                  149.7 |                           160.2 |              1 818.2% |
| Pottawattamie |                  200.6 |                           215.2 |              3 181.3% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                  147.3 |                           437.6 |              1 822.3% |
|   Crawford |                   63.4 |                           377.1 |              3 121.5% |
| Des Moines |                  132.9 |                           340.9 |              2 079.0% |
|    Webster |                  109.7 |                           305.6 |                724.4% |
|     Clarke |                   26.6 |                           282.8 |              2 043.9% |
|      Worth |                   20.4 |                           276.8 |              2 042.9% |
|     Wright |                   34.1 |                           271.8 |                969.5% |
|   Humboldt |                   25.4 |                           266.0 |                670.7% |
|    Calhoun |                   25.7 |                           266.0 |                939.1% |
|     Marion |                   86.0 |                           258.6 |              2 075.0% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|      Marshall |                   83.3 |                           211.6 |              6 454.1% |
|          Linn |                  470.3 |                           207.4 |              5 308.4% |
|    Washington |                   52.7 |                           240.0 |              4 076.8% |
|     Jefferson |                   38.4 |                           210.1 |              3 349.6% |
|         Scott |                  283.1 |                           163.7 |              3 329.2% |
|          Polk |                  935.0 |                           190.8 |              3 294.9% |
| Pottawattamie |                  200.6 |                           215.2 |              3 181.3% |
|        Warren |                  100.9 |                           196.0 |              3 140.8% |
|      Crawford |                   63.4 |                           377.1 |              3 121.5% |
|       Wapello |                   68.1 |                           194.9 |              2 924.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Adair |                    5.9 |                            81.9 |                166.7% |
|      Adams |                    3.7 |                           103.1 |                200.1% |
|    Decatur |                    7.9 |                            99.8 |                226.3% |
|     Monroe |                   13.6 |                           176.1 |                251.7% |
|   Ringgold |                    6.9 |                           140.1 |                400.1% |
|     Taylor |                    6.4 |                           105.0 |                477.7% |
|     Monona |                    9.0 |                           104.5 |                483.4% |
| Montgomery |                   13.6 |                           136.8 |                537.4% |
|   Hamilton |                   28.1 |                           190.5 |                558.0% |
|    Osceola |                    5.9 |                            98.3 |                585.7% |
