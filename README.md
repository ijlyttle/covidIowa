Compiled at 2021-06-02 00:56:27 UTC

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

## Tables as of 2021-06-01

As of 2021-06-01, IPDH is reporting 71 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-01 |                   87.0 |                             2.8 |               \-49.0% |
| 2021-05-31 |                  101.0 |                             3.2 |               \-42.2% |
| 2021-05-30 |                  108.9 |                             3.5 |               \-39.3% |
| 2021-05-29 |                  116.7 |                             3.7 |               \-36.0% |
| 2021-05-28 |                  128.9 |                             4.1 |               \-30.7% |
| 2021-05-27 |                  139.9 |                             4.4 |               \-29.0% |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   12.0 |                             2.4 |               \-53.3% |
|          Linn |                    6.4 |                             2.8 |               \-38.8% |
|         Scott |                    8.0 |                             4.6 |               \-34.4% |
|       Johnson |                    3.9 |                             2.6 |               \-22.7% |
|    Black Hawk |                    4.7 |                             3.6 |               \-35.5% |
|      Woodbury |                    2.4 |                             2.4 |               \-46.7% |
|       Dubuque |                    3.6 |                             3.7 |               \-25.6% |
|         Story |                    2.7 |                             2.8 |               \-39.5% |
|        Dallas |                    1.4 |                             1.5 |               \-66.7% |
| Pottawattamie |                    0.7 |                             0.8 |               \-62.5% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|       Adams |                    0.4 |                            11.9 |                  0.0% |
|       Davis |                    1.0 |                            11.1 |                  7.7% |
|         Ida |                    0.7 |                            10.4 |                 19.9% |
| Cerro Gordo |                    4.1 |                             9.8 |               \-39.0% |
|   Winnebago |                    1.0 |                             9.7 |                 40.0% |
|       Emmet |                    0.6 |                             6.2 |                  0.0% |
|  Des Moines |                    2.3 |                             5.9 |               \-47.7% |
|       Floyd |                    0.9 |                             5.5 |                  8.3% |
|   Muscatine |                    2.3 |                             5.4 |               \-30.3% |
|       Boone |                    1.3 |                             4.9 |               \-23.8% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|  Buchanan |                    0.7 |                             3.4 |                 50.0% |
|       Sac |                    0.4 |                             4.4 |                 42.9% |
| Winnebago |                    1.0 |                             9.7 |                 40.0% |
|    Marion |                    1.3 |                             3.9 |                 23.1% |
|       Ida |                    0.7 |                            10.4 |                 19.9% |
|    Shelby |                    0.1 |                             1.2 |                 14.3% |
| Appanoose |                    0.3 |                             2.3 |                 12.5% |
|    Greene |                    0.3 |                             3.2 |                 12.5% |
| Jefferson |                    0.4 |                             2.3 |                 11.1% |
|    Keokuk |                    0.4 |                             4.2 |                 11.1% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|        Dallas |                    1.4 |                             1.5 |               \-66.7% |
| Pottawattamie |                    0.7 |                             0.8 |               \-62.5% |
|       O’Brien |                  \-0.3 |                           \-2.1 |               \-58.3% |
|         Cedar |                    0.0 |                             0.0 |               \-56.3% |
|          Polk |                   12.0 |                             2.4 |               \-53.3% |
|       Carroll |                    0.0 |                             0.0 |               \-53.3% |
|      Delaware |                    0.0 |                             0.0 |               \-53.3% |
|       Clinton |                    1.3 |                             2.8 |               \-51.5% |
|       Hancock |                    0.0 |                             0.0 |               \-50.0% |
|        Warren |                    1.0 |                             1.9 |               \-48.1% |
