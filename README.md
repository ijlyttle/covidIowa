Compiled at 2021-05-29 00:29:48 UTC

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

## Tables as of 2021-05-28

As of 2021-05-28, IPDH is reporting 99 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   18.4 |                             3.8 |               \-41.1% |
|          Linn |                   10.6 |                             4.7 |               \-25.0% |
|         Scott |                    8.9 |                             5.1 |               \-40.0% |
|       Johnson |                    5.3 |                             3.5 |                \-6.4% |
|    Black Hawk |                    8.0 |                             6.1 |                 21.1% |
|      Woodbury |                    3.7 |                             3.6 |               \-31.3% |
|       Dubuque |                    5.7 |                             5.9 |                 17.5% |
|         Story |                    4.6 |                             4.7 |               \-13.3% |
|        Dallas |                    2.7 |                             2.9 |               \-48.0% |
| Pottawattamie |                    1.9 |                             2.0 |               \-58.3% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Cerro Gordo |                    6.6 |                            15.5 |                \-1.9% |
|         Ida |                    0.7 |                            10.4 |                 50.0% |
|     Jackson |                    1.9 |                             9.6 |                 17.6% |
|       Emmet |                    0.9 |                             9.3 |                 30.0% |
|      Louisa |                    1.0 |                             9.1 |                 40.0% |
|       Adams |                    0.3 |                             7.9 |               \-10.0% |
|         Lee |                    2.6 |                             7.6 |                 19.0% |
|    Franklin |                    0.7 |                             7.1 |               \-42.9% |
|  Des Moines |                    2.7 |                             7.0 |               \-51.9% |
|   Winnebago |                    0.7 |                             6.9 |                  0.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Winneshiek |                    0.6 |                             2.9 |                 83.3% |
|   Plymouth |                    1.3 |                             5.1 |                 77.8% |
|     Greene |                    0.4 |                             4.8 |                 66.7% |
|        Ida |                    0.7 |                            10.4 |                 50.0% |
|    Decatur |                    0.4 |                             5.5 |                 42.9% |
|     Louisa |                    1.0 |                             9.1 |                 40.0% |
|      Jones |                    1.3 |                             6.2 |                 33.4% |
|  Dickinson |                    0.7 |                             4.1 |                 33.3% |
|      Union |                    0.7 |                             5.8 |                 33.3% |
|   Buchanan |                    0.9 |                             4.0 |                 30.0% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Wright |                  \-0.6 |                           \-4.5 |               \-81.2% |
|         Henry |                    0.0 |                             0.0 |               \-68.2% |
|    Washington |                    0.1 |                             0.7 |               \-60.0% |
| Pottawattamie |                    1.9 |                             2.0 |               \-58.3% |
|     Palo Alto |                  \-0.1 |                           \-1.6 |               \-57.2% |
|         Boone |                    0.9 |                             3.3 |               \-56.7% |
|       Guthrie |                    0.0 |                             0.0 |               \-53.3% |
|    Des Moines |                    2.7 |                             7.0 |               \-51.9% |
|        Dallas |                    2.7 |                             2.9 |               \-48.0% |
|       Hancock |                    0.4 |                             4.0 |               \-44.4% |
