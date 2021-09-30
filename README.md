Compiled at 2021-09-30 17:26:56 UTC

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

## Tables as of 2021-09-28

As of 2021-09-28, IPDH is reporting 1.081210^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-28 |                 9174.1 |                           290.8 |                462.4% |
| 2021-09-21 |                 8325.6 |                           263.9 |                766.3% |
| 2021-09-14 |                 7098.0 |                           225.0 |              1 377.2% |
| 2021-09-08 |                  818.1 |                            25.9 |                308.7% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                 1514.4 |                           309.0 |                509.7% |
|          Linn |                  743.3 |                           327.9 |                580.2% |
|         Scott |                  406.6 |                           235.1 |                412.2% |
|       Johnson |                  326.0 |                           215.7 |                522.0% |
|    Black Hawk |                  320.9 |                           244.5 |                178.5% |
|      Woodbury |                  327.4 |                           317.6 |                471.9% |
|       Dubuque |                  178.6 |                           183.5 |                561.6% |
|         Story |                  176.3 |                           181.5 |                269.3% |
|        Dallas |                  230.7 |                           246.9 |                372.9% |
| Pottawattamie |                  271.7 |                           291.5 |                349.2% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Washington |                  110.4 |                           502.8 |                817.6% |
| Des Moines |                  188.6 |                           483.9 |                351.4% |
|        Lee |                  161.9 |                           480.9 |                160.9% |
|     Hardin |                   77.6 |                           460.5 |                467.0% |
|    Calhoun |                   44.4 |                           459.5 |                549.0% |
|     Clarke |                   40.0 |                           425.8 |                485.7% |
|       Clay |                   66.1 |                           413.0 |              1 578.6% |
|     Greene |                   36.3 |                           408.3 |                741.9% |
|      Worth |                   29.9 |                           404.5 |                440.0% |
|   Humboldt |                   37.9 |                           396.1 |                318.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|       Clay |                   66.1 |                           413.0 |              1 578.6% |
|      Union |                   33.1 |                           270.8 |              1 228.0% |
|   Mitchell |                   36.0 |                           340.1 |              1 195.1% |
| Montgomery |                   34.0 |                           342.8 |              1 189.6% |
|       Lyon |                   30.1 |                           256.4 |              1 182.1% |
|     Keokuk |                   38.3 |                           373.7 |                957.8% |
|       Page |                   46.9 |                           310.2 |                947.0% |
|  Poweshiek |                   48.0 |                           259.4 |                939.5% |
|  Dickinson |                   46.7 |                           270.7 |                912.2% |
|       Tama |                   54.9 |                           325.5 |                902.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Ida |                   20.7 |                           302.0 |                133.8% |
|     Butler |                   29.9 |                           206.8 |                142.7% |
|        Lee |                  161.9 |                           480.9 |                160.9% |
|    Webster |                  136.0 |                           378.8 |                172.4% |
|   Hamilton |                   39.0 |                           264.0 |                174.5% |
| Black Hawk |                  320.9 |                           244.5 |                178.5% |
|    Decatur |                   13.7 |                           174.3 |                202.9% |
|   Franklin |                   31.3 |                           310.7 |                213.9% |
|   Delaware |                   36.0 |                           211.6 |                219.8% |
|    Osceola |                    8.7 |                           146.3 |                223.8% |
