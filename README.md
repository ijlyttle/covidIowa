Compiled at 2021-06-04 18:23:49 UTC

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

## Tables as of 2021-06-04

As of 2021-06-04, IPDH is reporting 0 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-04 |                   84.3 |                             2.7 |               \-39.5% |
| 2021-06-02 |                  103.1 |                             3.3 |               \-32.9% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    9.4 |                             1.9 |               \-52.6% |
|          Linn |                    7.3 |                             3.2 |               \-25.6% |
|         Scott |                    7.7 |                             4.5 |               \-14.1% |
|       Johnson |                    2.9 |                             1.9 |               \-37.2% |
|    Black Hawk |                    6.3 |                             4.8 |               \-10.5% |
|      Woodbury |                    1.6 |                             1.5 |               \-52.6% |
|       Dubuque |                    3.3 |                             3.4 |               \-38.8% |
|         Story |                    2.0 |                             2.1 |               \-47.5% |
|        Dallas |                    2.1 |                             2.3 |               \-31.2% |
| Pottawattamie |                    2.3 |                             2.5 |                \-8.0% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Davis |                    1.0 |                            11.1 |                 16.7% |
|   Winnebago |                    0.9 |                             8.3 |                  8.3% |
|      Wright |                    1.0 |                             8.0 |                250.3% |
|       Adams |                    0.3 |                             7.9 |                  0.0% |
|     Audubon |                    0.4 |                             7.8 |               \-23.0% |
|  Washington |                    1.6 |                             7.2 |                 20.0% |
|  Des Moines |                    2.7 |                             7.0 |               \-16.1% |
| Cerro Gordo |                    2.9 |                             6.7 |               \-49.1% |
|       Emmet |                    0.6 |                             6.2 |               \-15.4% |
|      Clarke |                    0.6 |                             6.1 |                 37.4% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Wright |                    1.0 |                             8.0 |                250.3% |
| Winneshiek |                    0.7 |                             3.6 |                 71.4% |
|   Cherokee |                    0.4 |                             3.8 |                 66.7% |
|    Guthrie |                    0.6 |                             5.3 |                 37.4% |
|     Clarke |                    0.6 |                             6.1 |                 37.4% |
|  Palo Alto |                    0.1 |                             1.6 |                 33.4% |
|      Henry |                    0.7 |                             3.6 |                 33.3% |
|      Floyd |                    0.7 |                             4.6 |                 33.3% |
|     Monona |                    0.3 |                             3.3 |                 28.6% |
|       Cass |                    0.4 |                             3.3 |                 25.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Carroll |                  \-0.4 |                           \-2.1 |               \-63.7% |
|        Tama |                    0.0 |                             0.0 |               \-53.3% |
|        Polk |                    9.4 |                             1.9 |               \-52.6% |
|    Woodbury |                    1.6 |                             1.5 |               \-52.6% |
|     Wapello |                    0.1 |                             0.4 |               \-50.0% |
|     Jackson |                    0.4 |                             2.2 |               \-50.0% |
| Cerro Gordo |                    2.9 |                             6.7 |               \-49.1% |
|       Story |                    2.0 |                             2.1 |               \-47.5% |
|    Delaware |                    0.0 |                             0.0 |               \-46.1% |
|     O’Brien |                  \-0.3 |                           \-2.1 |               \-44.5% |
