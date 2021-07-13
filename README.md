Compiled at 2021-07-13 23:55:20 UTC

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

## Tables as of 2021-07-13

As of 2021-07-13, IPDH is reporting 163 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-13 |                  117.6 |                             3.7 |                 49.8% |
| 2021-07-12 |                  102.1 |                             3.2 |                 22.0% |
| 2021-07-11 |                   97.3 |                             3.1 |                 13.0% |
| 2021-07-10 |                   93.7 |                             3.0 |                 10.1% |
| 2021-07-09 |                   84.1 |                             2.7 |                \-1.3% |
| 2021-07-08 |                   79.3 |                             2.5 |                \-2.6% |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   41.7 |                             8.5 |                321.1% |
|          Linn |                   12.6 |                             5.5 |                196.9% |
|         Scott |                    3.1 |                             1.8 |                 20.8% |
|       Johnson |                    4.9 |                             3.2 |                105.0% |
|    Black Hawk |                   22.3 |                            17.0 |                 85.2% |
|      Woodbury |                  \-0.3 |                           \-0.3 |               \-78.3% |
|       Dubuque |                    4.6 |                             4.7 |                160.0% |
|         Story |                    6.3 |                             6.5 |                264.3% |
|        Dallas |                   11.9 |                            12.7 |                650.1% |
| Pottawattamie |                    2.6 |                             2.8 |                 38.9% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Jasper |                   40.4 |                           108.7 |              1 712.3% |
|    Decatur |                    3.7 |                            47.2 |                229.9% |
|    Fremont |                    2.7 |                            39.0 |                224.9% |
|     Monroe |                    2.7 |                            35.2 |                271.4% |
|      Henry |                    6.9 |                            34.4 |                323.1% |
|     Keokuk |                    3.4 |                            33.5 |                416.8% |
| Montgomery |                    2.7 |                            27.4 |                224.9% |
|   Franklin |                    2.7 |                            27.0 |                 85.7% |
|     Monona |                    2.3 |                            26.5 |                228.6% |
|   Humboldt |                    2.4 |                            25.4 |                 60.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|      Jasper |                   40.4 |                           108.7 |              1 712.3% |
|      Dallas |                   11.9 |                            12.7 |                650.1% |
|      Keokuk |                    3.4 |                            33.5 |                416.8% |
|       Henry |                    6.9 |                            34.4 |                323.1% |
|        Polk |                   41.7 |                             8.5 |                321.1% |
|  Washington |                    2.9 |                            13.0 |                285.7% |
|      Monroe |                    2.7 |                            35.2 |                271.4% |
|       Story |                    6.3 |                             6.5 |                264.3% |
| Buena Vista |                    3.0 |                            15.3 |                250.0% |
|     Decatur |                    3.7 |                            47.2 |                229.9% |

Biggest decline in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Iowa |                  \-3.3 |                          \-20.3 |              \-277.8% |
| Appanoose |                  \-2.3 |                          \-18.4 |              \-228.6% |
|   Mahaska |                  \-3.0 |                          \-13.6 |              \-227.3% |
|   Carroll |                  \-2.4 |                          \-12.0 |              \-225.0% |
|     Lucas |                  \-1.3 |                          \-15.0 |              \-128.6% |
|    Shelby |                  \-1.4 |                          \-12.5 |              \-125.0% |
|     Worth |                  \-1.1 |                          \-15.5 |              \-111.1% |
|   Audubon |                  \-1.1 |                          \-20.8 |              \-109.1% |
|     Mills |                  \-1.0 |                           \-6.6 |              \-100.0% |
|     Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
