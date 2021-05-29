Compiled at 2021-05-29 20:41:33 UTC

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

## Tables as of 2021-05-29

As of 2021-05-29, IPDH is reporting 85 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   16.1 |                             3.3 |               \-48.5% |
|          Linn |                    8.4 |                             3.7 |               \-33.3% |
|         Scott |                    8.4 |                             4.9 |               \-41.1% |
|       Johnson |                    5.6 |                             3.7 |                  2.2% |
|    Black Hawk |                    6.6 |                             5.0 |                  0.0% |
|      Woodbury |                    3.7 |                             3.6 |               \-28.3% |
|       Dubuque |                    5.6 |                             5.7 |                 35.3% |
|         Story |                    3.4 |                             3.5 |               \-29.5% |
|        Dallas |                    1.7 |                             1.8 |               \-66.7% |
| Pottawattamie |                    1.4 |                             1.5 |               \-58.5% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Ida |                    1.0 |                            14.6 |                 75.0% |
| Cerro Gordo |                    5.1 |                            12.1 |               \-29.5% |
|       Davis |                    1.0 |                            11.1 |               \-22.2% |
|      Louisa |                    1.0 |                             9.1 |                 16.7% |
|   Winnebago |                    0.9 |                             8.3 |                 18.2% |
|       Adams |                    0.3 |                             7.9 |               \-10.0% |
|       Emmet |                    0.7 |                             7.8 |                 19.9% |
|  Des Moines |                    3.0 |                             7.7 |               \-42.9% |
|         Lee |                    2.6 |                             7.6 |                 25.0% |
|       Jones |                    1.6 |                             7.6 |                 50.0% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Plymouth |                    1.3 |                             5.1 |                 77.8% |
|        Ida |                    1.0 |                            14.6 |                 75.0% |
| Winneshiek |                    0.4 |                             2.1 |                 66.7% |
|      Jones |                    1.6 |                             7.6 |                 50.0% |
|   Buchanan |                    0.9 |                             4.0 |                 44.4% |
|      Union |                    0.9 |                             7.0 |                 44.4% |
|     Keokuk |                    0.4 |                             4.2 |                 42.9% |
|     Greene |                    0.4 |                             4.8 |                 42.9% |
|    Dubuque |                    5.6 |                             5.7 |                 35.3% |
|       Page |                    0.7 |                             4.7 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Wright |                  \-0.6 |                           \-4.5 |               \-78.5% |
|        Dallas |                    1.7 |                             1.8 |               \-66.7% |
|       Carroll |                  \-0.1 |                           \-0.7 |               \-60.0% |
|         Henry |                    0.1 |                             0.7 |               \-60.0% |
| Pottawattamie |                    1.4 |                             1.5 |               \-58.5% |
|       Hancock |                    0.1 |                             1.3 |               \-55.5% |
|       Guthrie |                    0.0 |                             0.0 |               \-53.3% |
|     Muscatine |                    1.9 |                             4.4 |               \-50.0% |
|     Palo Alto |                    0.0 |                             0.0 |               \-50.0% |
|       Clinton |                    1.6 |                             3.4 |               \-48.6% |
