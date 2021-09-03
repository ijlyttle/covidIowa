Compiled at 2021-09-03 20:16:37 UTC

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

As of 2021-09-02, IPDH is reporting 8308 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-02 |                 4577.1 |                           145.1 |              2 401.7% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  725.4 |                           148.0 |              2 756.7% |
|          Linn |                  365.3 |                           161.1 |              4 738.0% |
|         Scott |                  234.9 |                           135.8 |              2 698.2% |
|       Johnson |                  165.3 |                           109.4 |              2 096.4% |
|    Black Hawk |                  264.3 |                           201.4 |              1 138.0% |
|      Woodbury |                  129.9 |                           125.9 |              1 661.4% |
|       Dubuque |                   82.1 |                            84.4 |              2 545.3% |
|         Story |                   98.7 |                           101.6 |              1 268.6% |
|        Dallas |                  123.3 |                           131.9 |              1 675.5% |
| Pottawattamie |                  167.3 |                           179.5 |              2 704.8% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                  122.0 |                           362.5 |              3 089.0% |
|    Crawford |                   52.9 |                           314.3 |              2 592.8% |
|  Des Moines |                  106.1 |                           272.4 |              1 729.3% |
|       Worth |                   19.6 |                           265.2 |              1 957.1% |
|     Webster |                   92.7 |                           258.2 |                583.3% |
|      Wright |                   28.9 |                           229.7 |                736.1% |
|    Humboldt |                   21.6 |                           225.7 |                618.1% |
|    Franklin |                   21.4 |                           212.8 |                726.4% |
| Buena Vista |                   40.6 |                           206.8 |              1 431.7% |
|      Marion |                   68.7 |                           206.6 |              1 642.8% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Linn |                  365.3 |                           161.1 |              4 738.0% |
|      Marshall |                   65.1 |                           165.5 |              4 110.2% |
|           Lee |                  122.0 |                           362.5 |              3 089.0% |
|    Washington |                   37.4 |                           170.4 |              2 888.3% |
|          Polk |                  725.4 |                           148.0 |              2 756.7% |
| Pottawattamie |                  167.3 |                           179.5 |              2 704.8% |
|         Scott |                  234.9 |                           135.8 |              2 698.2% |
|      Crawford |                   52.9 |                           314.3 |              2 592.8% |
|       Dubuque |                   82.1 |                            84.4 |              2 545.3% |
|     Jefferson |                   31.6 |                           172.6 |              2 432.7% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Adair |                    4.7 |                            65.9 |                135.2% |
|      Adams |                    3.6 |                            99.1 |                166.7% |
|     Monroe |                   10.4 |                           135.3 |                247.8% |
|    Decatur |                    7.1 |                            90.8 |                256.2% |
| Montgomery |                    8.1 |                            82.1 |                276.4% |
|    Calhoun |                   17.3 |                           178.8 |                433.3% |
|     Monona |                    8.4 |                            97.8 |                450.1% |
|    Osceola |                    4.6 |                            76.7 |                457.1% |
|       Cass |                   12.7 |                            99.0 |                464.6% |
|    Hancock |                   12.7 |                           119.6 |                464.6% |
