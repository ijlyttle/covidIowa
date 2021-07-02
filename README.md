Compiled at 2021-07-02 17:25:22 UTC

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

## Tables as of 2021-07-02

As of 2021-07-02, IPDH is reporting 96 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    9.6 |                             2.0 |                 17.5% |
|          Linn |                    4.4 |                             2.0 |               \-28.3% |
|         Scott |                    3.0 |                             1.7 |                 64.7% |
|       Johnson |                    3.3 |                             2.2 |                 87.5% |
|    Black Hawk |                   14.0 |                            10.7 |                \-3.7% |
|      Woodbury |                    2.1 |                             2.1 |                100.1% |
|       Dubuque |                    2.4 |                             2.5 |                 26.3% |
|         Story |                    1.3 |                             1.3 |                 14.3% |
|        Dallas |                    0.9 |                             0.9 |               \-18.8% |
| Pottawattamie |                    1.6 |                             1.7 |                  0.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    5.3 |                            14.7 |                 63.0% |
|   Humboldt |                    1.3 |                            13.5 |                128.6% |
|      Wayne |                    0.9 |                            13.3 |                 85.7% |
| Black Hawk |                   14.0 |                            10.7 |                \-3.7% |
|        Lee |                    3.6 |                            10.6 |                128.6% |
|      Adams |                    0.3 |                             7.9 |                  0.0% |
| Winneshiek |                    1.6 |                             7.9 |                 38.4% |
|    Audubon |                    0.4 |                             7.8 |                 66.7% |
|    Calhoun |                    0.7 |                             7.4 |                 50.0% |
|     Hardin |                    1.1 |                             6.8 |                 87.5% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Lee |                    3.6 |                            10.6 |                128.6% |
|    Humboldt |                    1.3 |                            13.5 |                128.6% |
|    Woodbury |                    2.1 |                             2.1 |                100.1% |
| Buena Vista |                    0.7 |                             3.6 |                100.0% |
|     Johnson |                    3.3 |                             2.2 |                 87.5% |
|      Hardin |                    1.1 |                             6.8 |                 87.5% |
|       Wayne |                    0.9 |                            13.3 |                 85.7% |
| Cerro Gordo |                    1.9 |                             4.4 |                 81.9% |
|     Wapello |                    1.3 |                             3.7 |                 77.8% |
|    Crawford |                    0.4 |                             2.6 |                 66.7% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monona |                  \-0.1 |                           \-1.7 |               \-60.0% |
|    Sioux |                    0.0 |                             0.0 |               \-50.0% |
| Buchanan |                    0.0 |                             0.0 |               \-46.1% |
|    Henry |                    0.3 |                             1.4 |               \-35.7% |
|    Adair |                    0.0 |                             0.0 |               \-30.0% |
|     Linn |                    4.4 |                             2.0 |               \-28.3% |
|  Mahaska |                    0.1 |                             0.6 |               \-27.2% |
|    Cedar |                    0.0 |                             0.0 |               \-22.2% |
|   Howard |                    0.0 |                             0.0 |               \-22.2% |
|   Monroe |                    0.0 |                             0.0 |               \-22.2% |
