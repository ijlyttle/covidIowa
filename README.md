Compiled at 2021-09-20 20:18:37 UTC

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

## Tables as of 2021-09-14

As of 2021-09-14, IPDH is reporting 4.611610^{4} new cases since the
previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-09-14 |                 7098.0 |                           225.0 |              1 377.2% |
| 2021-09-08 |                  818.1 |                            25.9 |                308.7% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                 1160.9 |                           236.8 |              1 573.4% |
|          Linn |                  590.1 |                           260.3 |              2 291.9% |
|         Scott |                  328.3 |                           189.8 |              1 396.8% |
|       Johnson |                  257.3 |                           170.2 |              1 485.9% |
|    Black Hawk |                  324.4 |                           247.2 |                649.3% |
|      Woodbury |                  223.1 |                           216.4 |              1 313.5% |
|       Dubuque |                  131.4 |                           135.1 |              1 526.3% |
|         Story |                  135.1 |                           139.2 |                557.3% |
|        Dallas |                  177.1 |                           189.6 |                956.8% |
| Pottawattamie |                  237.9 |                           255.2 |              1 227.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                  163.0 |                           484.3 |              1 161.5% |
| Des Moines |                  161.0 |                           413.2 |              1 475.0% |
|   Crawford |                   68.7 |                           408.5 |              1 034.9% |
| Washington |                   78.1 |                           355.8 |              2 538.1% |
|    Calhoun |                   33.6 |                           347.2 |                633.4% |
|     Clarke |                   32.0 |                           340.6 |              2 000.6% |
|    Webster |                  120.1 |                           334.6 |                430.0% |
|     Marion |                  109.6 |                           329.5 |              1 234.4% |
|     Hardin |                   54.7 |                           324.8 |              1 081.9% |
|   Humboldt |                   30.3 |                           316.9 |                476.3% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Jones |                   42.6 |                           205.8 |              2 949.1% |
| Washington |                   78.1 |                           355.8 |              2 538.1% |
|       Linn |                  590.1 |                           260.3 |              2 291.9% |
|   Marshall |                  100.9 |                           256.2 |              2 276.5% |
|       Page |                   37.0 |                           244.9 |              2 117.0% |
|      Union |                   21.0 |                           171.6 |              2 100.0% |
|     Warren |                  130.9 |                           254.3 |              2 097.6% |
|      Henry |                   54.6 |                           273.5 |              2 061.5% |
|     Clarke |                   32.0 |                           340.6 |              2 000.6% |
|    Jackson |                   28.7 |                           147.7 |              1 979.4% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|    Adair |                    7.4 |                           103.9 |                195.0% |
|   Monroe |                   18.0 |                           233.6 |                280.0% |
|  Audubon |                    6.9 |                           124.8 |                292.9% |
|  Osceola |                    6.0 |                           100.7 |                308.4% |
| Ringgold |                    7.3 |                           148.9 |                314.3% |
| Hamilton |                   32.1 |                           217.6 |                329.6% |
|    Adams |                    5.9 |                           162.6 |                336.5% |
|   Monona |                   11.4 |                           132.7 |                383.4% |
|  Decatur |                   11.6 |                           147.0 |                389.0% |
|    Davis |                   20.9 |                           231.7 |                393.5% |
