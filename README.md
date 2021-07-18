Compiled at 2021-07-18 23:53:27 UTC

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

## Tables as of 2021-07-18

As of 2021-07-18, IPDH is reporting 101 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   18.3 |                             3.7 |               \-52.5% |
|          Linn |                    5.0 |                             2.2 |               \-56.2% |
|         Scott |                    7.7 |                             4.5 |                306.6% |
|       Johnson |                    6.1 |                             4.1 |                 31.6% |
|    Black Hawk |                   18.0 |                            13.7 |                \-8.3% |
|      Woodbury |                    6.3 |                             6.1 |              \-950.2% |
|       Dubuque |                    1.7 |                             1.8 |               \-48.7% |
|         Story |                    3.9 |                             4.0 |               \-35.8% |
|        Dallas |                    3.6 |                             3.8 |               \-62.4% |
| Pottawattamie |                    3.9 |                             4.1 |                 79.0% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monroe |                    2.6 |                            33.4 |                  8.7% |
|  Calhoun |                    2.9 |                            29.6 |                 28.6% |
|  Webster |                   10.4 |                            29.0 |                 45.5% |
| Franklin |                    2.1 |                            21.3 |               \-12.0% |
|   Wright |                    2.6 |                            20.5 |                212.4% |
| Humboldt |                    1.9 |                            19.4 |               \-13.1% |
| Hamilton |                    2.9 |                            19.3 |                 22.7% |
|  Hancock |                    1.9 |                            17.5 |                 17.6% |
|  Decatur |                    1.3 |                            16.3 |               \-48.4% |
|    Adair |                    1.1 |                            16.0 |                  0.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Mills |                    0.0 |                             0.0 |                   Inf |
|      Union |                    0.0 |                             0.0 |                   Inf |
|      Worth |                    0.0 |                             0.0 |                   Inf |
|    Audubon |                    0.0 |                             0.0 |                   Inf |
|      Adams |                    0.6 |                            15.9 |                   Inf |
|       Cass |                    2.0 |                            15.6 |                320.2% |
|      Scott |                    7.7 |                             4.5 |                306.6% |
| Winneshiek |                    0.7 |                             3.6 |                299.5% |
|     Marion |                    2.0 |                             6.0 |                250.1% |
|     Wright |                    2.6 |                            20.5 |                212.4% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Woodbury |                    6.3 |                             6.1 |              \-950.2% |
|     Lucas |                    0.4 |                             5.0 |              \-599.7% |
|    Shelby |                    1.3 |                            11.2 |              \-420.2% |
|   Carroll |                    0.7 |                             3.5 |              \-219.9% |
| Appanoose |                    0.3 |                             2.3 |              \-200.0% |
|   Mahaska |                    1.1 |                             5.2 |              \-193.7% |
|      Iowa |                    0.1 |                             0.9 |              \-150.0% |
|    Jasper |                    1.6 |                             4.2 |               \-93.8% |
|     Henry |                    0.4 |                             2.1 |               \-81.5% |
|   Fremont |                    0.1 |                             2.1 |               \-69.2% |
