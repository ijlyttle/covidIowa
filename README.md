Compiled at 2021-07-15 23:54:01 UTC

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

## Tables as of 2021-07-15

As of 2021-07-15, IPDH is reporting 196 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-15 |                  139.6 |                             4.4 |                 75.1% |
| 2021-07-14 |                  131.4 |                             4.2 |                 71.0% |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   18.1 |                             3.7 |               \-51.1% |
|          Linn |                    6.1 |                             2.7 |               \-36.7% |
|         Scott |                    6.0 |                             3.5 |                206.2% |
|       Johnson |                    2.1 |                             1.4 |               \-35.3% |
|    Black Hawk |                   16.1 |                            12.3 |               \-10.4% |
|      Woodbury |                    5.0 |                             4.8 |              \-624.9% |
|       Dubuque |                    1.9 |                             1.9 |               \-42.9% |
|         Story |                    1.9 |                             1.9 |               \-62.3% |
|        Dallas |                    3.3 |                             3.5 |               \-61.0% |
| Pottawattamie |                    3.3 |                             3.5 |                114.3% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                   10.0 |                            27.9 |                 71.1% |
|    Calhoun |                    2.3 |                            23.6 |                 15.0% |
|      Adams |                    0.7 |                            19.8 |                   Inf |
|   Franklin |                    1.9 |                            18.4 |               \-23.1% |
|     Wright |                    2.3 |                            18.2 |                360.2% |
|    Decatur |                    1.4 |                            18.2 |               \-43.3% |
|    Hancock |                    1.7 |                            16.1 |                 46.1% |
|     Monona |                    1.3 |                            14.9 |               \-11.1% |
|     Monroe |                    1.1 |                            14.8 |               \-28.6% |
| Montgomery |                    1.4 |                            14.4 |               \-22.7% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Audubon |                    0.0 |                             0.0 |                   Inf |
|         Adams |                    0.7 |                            19.8 |                   Inf |
|        Wright |                    2.3 |                            18.2 |                360.2% |
|    Winneshiek |                    0.6 |                             2.9 |                266.2% |
|         Mills |                    0.0 |                             0.0 |                249.7% |
|         Scott |                    6.0 |                             3.5 |                206.2% |
|          Cass |                    1.4 |                            11.1 |                183.4% |
|      Mitchell |                    1.0 |                             9.4 |                180.1% |
|      Ringgold |                    0.3 |                             5.8 |                125.2% |
| Pottawattamie |                    3.3 |                             3.5 |                114.3% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Union |                    0.3 |                             2.3 |              \-999.3% |
|    Marion |                    2.9 |                             8.6 |              \-999.1% |
|     Worth |                    0.1 |                             1.9 |              \-899.3% |
|  Woodbury |                    5.0 |                             4.8 |              \-624.9% |
|     Lucas |                    0.3 |                             3.3 |              \-549.7% |
|    Shelby |                    1.1 |                            10.0 |              \-475.3% |
|   Mahaska |                    0.9 |                             3.9 |              \-200.0% |
|   Carroll |                    0.6 |                             2.8 |              \-200.0% |
| Appanoose |                    0.0 |                             0.0 |              \-177.8% |
|      Iowa |                    0.0 |                             0.0 |              \-150.0% |
