Compiled at 2021-07-23 17:25:27 UTC

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

## Tables as of 2021-07-21

As of 2021-07-21, IPDH is reporting 324 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |
| 2021-07-18 |                  157.7 |                             5.0 |                 61.5% |
| 2021-07-17 |                  155.6 |                             4.9 |                 65.3% |
| 2021-07-16 |                  150.4 |                             4.8 |                 77.9% |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   26.6 |                             5.4 |               \-38.9% |
|          Linn |                    7.7 |                             3.4 |               \-34.4% |
|         Scott |                    7.3 |                             4.2 |                 52.6% |
|       Johnson |                    7.3 |                             4.8 |                 75.8% |
|    Black Hawk |                   20.6 |                            15.7 |                \-6.2% |
|      Woodbury |                    7.4 |                             7.2 |                489.9% |
|       Dubuque |                    2.7 |                             2.8 |               \-33.3% |
|         Story |                    6.3 |                             6.5 |               \-12.1% |
|        Dallas |                    6.9 |                             7.3 |               \-40.9% |
| Pottawattamie |                    5.1 |                             5.5 |                 79.1% |

Most positive-cases, per-capita:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monroe |                    3.1 |                            40.8 |                  7.4% |
|  Webster |                   12.4 |                            34.6 |                 20.5% |
| Humboldt |                    2.4 |                            25.4 |                \-7.7% |
| Hamilton |                    3.4 |                            23.2 |                 14.8% |
|    Adair |                    1.6 |                            22.0 |                 12.5% |
|  Decatur |                    1.7 |                            21.8 |               \-40.6% |
|      Lee |                    6.7 |                            19.9 |                125.0% |
| Franklin |                    2.0 |                            19.9 |               \-22.2% |
|   Wright |                    2.3 |                            18.2 |                 53.3% |
|  Kossuth |                    2.4 |                            16.4 |                 41.2% |

Most growth in positive cases, week-over-week:

    #> Warning: One or more parsing issues, see `problems()` for details

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Winneshiek |                    0.7 |                             3.6 |                499.3% |
|   Woodbury |                    7.4 |                             7.2 |                489.9% |
|      Adams |                    0.6 |                            15.9 |                266.2% |
|     Butler |                    1.0 |                             6.9 |                180.1% |
|   Ringgold |                    0.6 |                            11.7 |                175.1% |
|      Jones |                    0.3 |                             1.4 |                125.2% |
|        Lee |                    6.7 |                            19.9 |                125.0% |
|    Fayette |                    0.6 |                             2.9 |                120.0% |
|     Marion |                    3.0 |                             9.0 |                115.4% |
|      Boone |                    2.9 |                            10.9 |                107.7% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Worth |                    0.0 |                             0.0 |              \-799.3% |
|   Audubon |                    0.0 |                             0.0 |              \-799.3% |
|    Shelby |                    0.7 |                             6.2 |              \-699.3% |
|     Lucas |                    0.4 |                             5.0 |              \-599.7% |
|   Carroll |                    0.4 |                             2.1 |              \-242.9% |
| Appanoose |                    0.7 |                             5.7 |              \-233.3% |
|   Mahaska |                    1.7 |                             7.8 |              \-211.7% |
|      Iowa |                    0.6 |                             3.5 |              \-173.3% |
|    Jasper |                    1.7 |                             4.6 |               \-93.5% |
|     Henry |                    0.7 |                             3.6 |               \-77.8% |
