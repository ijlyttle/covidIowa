Compiled at 2021-08-30 17:28:05 UTC

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

## Tables as of 2021-08-26

As of 2021-08-26, IPDH is reporting 7112 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  527.1 |                           107.5 |              2 300.7% |
|          Linn |                  266.7 |                           117.6 |              4 064.2% |
|         Scott |                  180.0 |                           104.1 |              1 819.6% |
|       Johnson |                  117.4 |                            77.7 |              1 494.1% |
|    Black Hawk |                  218.4 |                           166.4 |              1 005.0% |
|      Woodbury |                   97.1 |                            94.2 |              1 126.8% |
|       Dubuque |                   62.1 |                            63.9 |              1 909.0% |
|         Story |                   78.1 |                            80.5 |              1 357.8% |
|        Dallas |                   95.4 |                           102.1 |              1 587.6% |
| Pottawattamie |                  128.6 |                           137.9 |              2 112.2% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                  100.9 |                           299.7 |              2 642.5% |
|   Crawford |                   39.0 |                           231.9 |              1 766.5% |
|    Webster |                   79.4 |                           221.2 |                547.1% |
| Des Moines |                   83.6 |                           214.5 |              1 276.7% |
|      Worth |                   13.0 |                           176.1 |              1 300.0% |
|     Wright |                   21.9 |                           174.0 |                595.6% |
|   Humboldt |                   16.6 |                           173.4 |                515.0% |
|        Ida |                   11.4 |                           166.6 |                987.4% |
| Black Hawk |                  218.4 |                           166.4 |              1 005.0% |
|   Franklin |                   16.1 |                           160.3 |                471.4% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Linn |                  266.7 |                           117.6 |              4 064.2% |
|      Marshall |                   46.9 |                           119.0 |              2 946.3% |
|           Lee |                  100.9 |                           299.7 |              2 642.5% |
|          Polk |                  527.1 |                           107.5 |              2 300.7% |
| Pottawattamie |                  128.6 |                           137.9 |              2 112.2% |
|       Dubuque |                   62.1 |                            63.9 |              1 909.0% |
|        Benton |                   26.7 |                           104.2 |              1 839.4% |
|       Fayette |                   23.9 |                           121.4 |              1 832.9% |
|         Scott |                  180.0 |                           104.1 |              1 819.6% |
|    Washington |                   26.3 |                           119.7 |              1 809.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Adair |                    3.4 |                            47.9 |                 82.3% |
| Montgomery |                    4.6 |                            46.1 |                129.4% |
|    Decatur |                    5.4 |                            69.0 |                181.2% |
|     Monroe |                    8.4 |                           109.4 |                186.9% |
|      Adams |                    3.1 |                            87.3 |                189.9% |
|    Calhoun |                   10.1 |                           104.9 |                212.0% |
|     Monona |                    4.9 |                            56.4 |                241.7% |
|    Hancock |                    8.7 |                            82.0 |                257.9% |
| Pocahontas |                    3.7 |                            56.1 |                266.6% |
|       Cass |                   10.6 |                            82.4 |                305.0% |
