Compiled at 2021-07-07 20:15:03 UTC

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

## Tables as of 2021-07-07

As of 2021-07-07, IPDH is reporting 105 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-07 |                   76.4 |                             2.4 |                  4.2% |
| 2021-07-06 |                   78.1 |                             2.5 |                  8.0% |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    9.1 |                             1.9 |                 14.5% |
|          Linn |                    3.7 |                             1.6 |               \-13.2% |
|         Scott |                    2.3 |                             1.3 |               \-11.5% |
|       Johnson |                    2.7 |                             1.8 |                 23.8% |
|    Black Hawk |                   12.7 |                             9.7 |                \-5.9% |
|      Woodbury |                    1.6 |                             1.5 |                  0.0% |
|       Dubuque |                    1.0 |                             1.0 |               \-44.0% |
|         Story |                    0.7 |                             0.7 |               \-25.0% |
|        Dallas |                    0.6 |                             0.6 |               \-31.3% |
| Pottawattamie |                    2.0 |                             2.1 |                 50.0% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    5.1 |                            14.3 |                 13.2% |
|    Calhoun |                    1.3 |                            13.3 |                 60.0% |
|   Franklin |                    1.1 |                            11.4 |                 87.5% |
| Black Hawk |                   12.7 |                             9.7 |                \-5.9% |
|    Decatur |                    0.7 |                             9.1 |                  9.1% |
|   Humboldt |                    0.9 |                             9.0 |                \-7.2% |
|        Lee |                    3.0 |                             8.9 |                 27.3% |
|      Wayne |                    0.6 |                             8.9 |                  0.0% |
|    Audubon |                    0.4 |                             7.8 |                 66.7% |
|  Allamakee |                    0.9 |                             6.3 |                 85.7% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|       Mahaska |                    1.3 |                             5.8 |                100.0% |
|      Franklin |                    1.1 |                            11.4 |                 87.5% |
|     Allamakee |                    0.9 |                             6.3 |                 85.7% |
|       Audubon |                    0.4 |                             7.8 |                 66.7% |
|       Calhoun |                    1.3 |                            13.3 |                 60.0% |
|      Hamilton |                    0.6 |                             3.9 |                 57.1% |
|    Des Moines |                    2.3 |                             5.9 |                 53.3% |
| Pottawattamie |                    2.0 |                             2.1 |                 50.0% |
|        Shelby |                    0.7 |                             6.2 |                 50.0% |
|        Butler |                    0.9 |                             5.9 |                 44.4% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Winneshiek |                    0.4 |                             2.1 |               \-54.5% |
|      Hardin |                    0.1 |                             0.8 |               \-46.7% |
|     Dubuque |                    1.0 |                             1.0 |               \-44.0% |
|        Lyon |                    0.1 |                             1.2 |               \-42.8% |
|      Benton |                    0.6 |                             2.2 |               \-35.3% |
|      Wright |                    0.1 |                             1.1 |               \-33.3% |
|      Dallas |                    0.6 |                             0.6 |               \-31.3% |
|     Carroll |                    0.0 |                             0.0 |               \-30.0% |
| Buena Vista |                    0.0 |                             0.0 |               \-30.0% |
|    Cherokee |                    0.1 |                             1.3 |               \-27.2% |
