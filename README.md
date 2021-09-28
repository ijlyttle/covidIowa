Compiled at 2021-09-28 17:24:24 UTC

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

## Tables as of 2021-09-21

As of 2021-09-21, IPDH is reporting 1.216310^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-21 |                 8325.6 |                           263.9 |                766.3% |
| 2021-09-14 |                 7098.0 |                           225.0 |              1 377.2% |
| 2021-09-08 |                  818.1 |                            25.9 |                308.7% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                 1384.4 |                           282.4 |                871.7% |
|          Linn |                  688.9 |                           303.9 |              1 119.5% |
|         Scott |                  373.4 |                           215.9 |                729.4% |
|       Johnson |                  297.4 |                           196.8 |                885.4% |
|    Black Hawk |                  326.1 |                           248.5 |                324.1% |
|      Woodbury |                  279.3 |                           270.9 |                681.7% |
|       Dubuque |                  157.9 |                           162.2 |              1 034.7% |
|         Story |                  156.1 |                           160.8 |                370.1% |
|        Dallas |                  204.9 |                           219.2 |                558.0% |
| Pottawattamie |                  267.0 |                           286.5 |                712.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                  163.1 |                           484.7 |                328.7% |
| Des Moines |                  176.3 |                           452.4 |                529.9% |
| Washington |                   96.0 |                           437.1 |              1 516.7% |
|     Hardin |                   71.1 |                           422.3 |                852.9% |
|   Crawford |                   70.7 |                           420.4 |                569.3% |
|     Clarke |                   37.4 |                           398.4 |              1 020.7% |
|     Louisa |                   42.7 |                           387.1 |              1 290.8% |
|    Calhoun |                   37.3 |                           385.7 |                523.2% |
|    Webster |                  130.7 |                           364.1 |                273.3% |
|     Marion |                  119.9 |                           360.4 |                531.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Mitchell |                   26.9 |                           253.7 |              2 337.2% |
|       Clay |                   53.3 |                           332.7 |              2 011.5% |
|    Jackson |                   39.1 |                           201.4 |              1 773.2% |
|      Jones |                   55.0 |                           265.9 |              1 604.2% |
|       Page |                   41.9 |                           277.1 |              1 566.9% |
| Washington |                   96.0 |                           437.1 |              1 516.7% |
|      Union |                   28.3 |                           231.1 |              1 477.1% |
|   Marshall |                  128.9 |                           327.3 |              1 390.2% |
|  Poweshiek |                   41.0 |                           221.6 |              1 370.1% |
|     Louisa |                   42.7 |                           387.1 |              1 290.8% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|      Ida |                   19.6 |                           285.3 |                220.0% |
|    Adair |                   10.0 |                           139.8 |                220.8% |
| Ringgold |                    7.9 |                           160.5 |                244.5% |
|    Davis |                   21.7 |                           241.3 |                261.3% |
|    Adams |                    9.4 |                           261.8 |                265.0% |
| Hamilton |                   36.1 |                           244.7 |                266.2% |
|  Webster |                  130.7 |                           364.1 |                273.3% |
|  Audubon |                    8.7 |                           158.6 |                277.8% |
|   Butler |                   28.6 |                           197.9 |                290.6% |
|   Monroe |                   23.4 |                           304.0 |                307.1% |
