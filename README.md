Compiled at 2021-06-14 23:53:56 UTC

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

## Tables as of 2021-06-14

As of 2021-06-14, IPDH is reporting 66 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |
| 2021-06-09 |                  113.0 |                             3.6 |                 29.5% |
| 2021-06-08 |                  107.6 |                             3.4 |                  6.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   12.7 |                             2.6 |                \-4.0% |
|          Linn |                    7.6 |                             3.3 |               \-35.5% |
|         Scott |                    2.9 |                             1.7 |               \-40.0% |
|       Johnson |                    2.4 |                             1.6 |               \-22.6% |
|    Black Hawk |                   13.7 |                            10.5 |                 47.1% |
|      Woodbury |                    2.3 |                             2.2 |                 15.0% |
|       Dubuque |                    3.1 |                             3.2 |               \-21.6% |
|         Story |                    1.0 |                             1.0 |               \-22.2% |
|        Dallas |                    2.1 |                             2.3 |               \-26.7% |
| Pottawattamie |                    2.6 |                             2.8 |               \-19.4% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    1.0 |                            18.2 |                  7.7% |
|    Ringgold |                    0.6 |                            11.7 |                 57.1% |
|  Black Hawk |                   13.7 |                            10.5 |                 47.1% |
|      Taylor |                    0.4 |                             7.0 |                 42.9% |
| Cerro Gordo |                    2.9 |                             6.7 |                 35.0% |
|      Shelby |                    0.7 |                             6.2 |                140.1% |
|       Cedar |                    1.1 |                             6.1 |                 87.5% |
|    Hamilton |                    0.9 |                             5.8 |                 44.4% |
|        Page |                    0.9 |                             5.7 |                  8.3% |
|         Lee |                    1.7 |                             5.1 |               \-17.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Shelby |                    0.7 |                             6.2 |                140.1% |
|      Cedar |                    1.1 |                             6.1 |                 87.5% |
|      Mills |                    0.7 |                             4.7 |                 71.4% |
|    Webster |                    1.7 |                             4.8 |                 58.3% |
|   Ringgold |                    0.6 |                            11.7 |                 57.1% |
|   Buchanan |                    1.0 |                             4.7 |                 55.5% |
| Black Hawk |                   13.7 |                            10.5 |                 47.1% |
|       Tama |                    0.9 |                             5.1 |                 44.4% |
|   Hamilton |                    0.9 |                             5.8 |                 44.4% |
|     Taylor |                    0.4 |                             7.0 |                 42.9% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                  \-0.6 |                           \-2.8 |               \-66.6% |
| Buena Vista |                  \-0.1 |                           \-0.7 |               \-50.0% |
|  Des Moines |                    0.9 |                             2.2 |               \-45.8% |
|       Union |                    0.1 |                             1.2 |               \-42.8% |
|    Franklin |                    0.1 |                             1.4 |               \-42.8% |
|  Washington |                    0.6 |                             2.6 |               \-42.1% |
|       Scott |                    2.9 |                             1.7 |               \-40.0% |
|   Winnebago |                    0.1 |                             1.4 |               \-38.4% |
|   Appanoose |                    0.0 |                             0.0 |               \-36.3% |
|        Linn |                    7.6 |                             3.3 |               \-35.5% |
