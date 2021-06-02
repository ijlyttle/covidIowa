Compiled at 2021-06-02 21:26:27 UTC

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

## Tables as of 2021-06-02

As of 2021-06-02, IPDH is reporting 169 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-02 |                   88.0 |                             2.8 |               \-42.7% |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.3 |                             2.3 |               \-52.7% |
|          Linn |                    7.9 |                             3.5 |               \-26.2% |
|         Scott |                    8.0 |                             4.6 |               \-25.0% |
|       Johnson |                    3.3 |                             2.2 |               \-31.8% |
|    Black Hawk |                    6.4 |                             4.9 |               \-10.3% |
|      Woodbury |                    2.1 |                             2.1 |               \-37.1% |
|       Dubuque |                    3.4 |                             3.5 |               \-40.4% |
|         Story |                    2.6 |                             2.6 |               \-41.9% |
|        Dallas |                    2.0 |                             2.1 |               \-44.7% |
| Pottawattamie |                    1.4 |                             1.5 |               \-37.0% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Adams |                    0.4 |                            11.9 |                 11.1% |
|         Ida |                    0.7 |                            10.4 |                  9.1% |
|       Davis |                    0.9 |                             9.5 |                  8.3% |
|       Emmet |                    0.9 |                             9.3 |                  8.3% |
|   Winnebago |                    0.9 |                             8.3 |                 18.2% |
|  Des Moines |                    3.1 |                             8.1 |                \-9.4% |
|      Louisa |                    0.7 |                             6.5 |                 19.9% |
| Cerro Gordo |                    2.7 |                             6.4 |               \-53.6% |
|      Bremer |                    1.6 |                             6.3 |                 79.9% |
|   Van Buren |                    0.4 |                             6.1 |                 66.7% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|    Shelby |                    0.3 |                             2.5 |                 80.1% |
|    Bremer |                    1.6 |                             6.3 |                 79.9% |
| Van Buren |                    0.4 |                             6.1 |                 66.7% |
|  Cherokee |                    0.3 |                             2.5 |                 50.1% |
|    Wright |                    0.6 |                             4.5 |                 37.4% |
|  Buchanan |                    0.7 |                             3.4 |                 33.3% |
|   Webster |                    0.9 |                             2.4 |                 30.0% |
|    Keokuk |                    0.3 |                             2.8 |                 28.6% |
|    Benton |                    1.0 |                             3.9 |                 27.3% |
|    Louisa |                    0.7 |                             6.5 |                 19.9% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|  Washington |                    0.1 |                             0.7 |               \-60.0% |
|     Madison |                    0.1 |                             0.9 |               \-60.0% |
|        Tama |                    0.0 |                             0.0 |               \-56.3% |
|     O’Brien |                  \-0.3 |                           \-2.1 |               \-54.6% |
| Cerro Gordo |                    2.7 |                             6.4 |               \-53.6% |
|     Clayton |                    0.0 |                             0.0 |               \-53.3% |
|    Delaware |                    0.0 |                             0.0 |               \-53.3% |
|        Polk |                   11.3 |                             2.3 |               \-52.7% |
|       Boone |                    0.7 |                             2.7 |               \-52.0% |
|        Iowa |                    0.0 |                             0.0 |               \-50.0% |
