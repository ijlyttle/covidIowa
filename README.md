Compiled at 2021-06-16 23:54:27 UTC

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

## Tables as of 2021-06-16

As of 2021-06-16, IPDH is reporting 183 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-16 |                   83.0 |                             2.6 |               \-26.3% |
| 2021-06-15 |                   72.4 |                             2.3 |               \-32.4% |
| 2021-06-14 |                   82.3 |                             2.6 |               \-15.6% |
| 2021-06-13 |                   78.6 |                             2.5 |               \-21.7% |
| 2021-06-12 |                   81.9 |                             2.6 |               \-19.2% |
| 2021-06-11 |                   79.1 |                             2.5 |               \-20.9% |
| 2021-06-10 |                   83.7 |                             2.7 |               \-18.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   11.3 |                             2.3 |               \-35.8% |
|          Linn |                    7.9 |                             3.5 |               \-36.1% |
|         Scott |                    3.6 |                             2.1 |               \-28.9% |
|       Johnson |                    2.6 |                             1.7 |               \-16.7% |
|    Black Hawk |                   14.1 |                            10.8 |                 17.8% |
|      Woodbury |                    2.7 |                             2.6 |                 18.2% |
|       Dubuque |                    3.4 |                             3.5 |               \-16.2% |
|         Story |                    0.9 |                             0.9 |               \-38.1% |
|        Dallas |                    1.9 |                             2.0 |               \-41.2% |
| Pottawattamie |                    2.0 |                             2.1 |               \-43.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|     Audubon |                    0.7 |                            13.0 |               \-36.8% |
|  Black Hawk |                   14.1 |                            10.8 |                 17.8% |
|      Taylor |                    0.6 |                             9.3 |                 57.1% |
|    Ringgold |                    0.4 |                             8.8 |                 25.0% |
|      Monroe |                    0.6 |                             7.4 |                 37.4% |
| Cerro Gordo |                    2.7 |                             6.4 |                  8.3% |
|    Buchanan |                    1.3 |                             6.1 |                 45.5% |
| Buena Vista |                    1.0 |                             5.1 |                  7.7% |
|      Benton |                    1.3 |                             5.0 |                  0.0% |
|       Mills |                    0.7 |                             4.7 |                 71.4% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|   Carroll |                    0.6 |                             2.8 |                 83.3% |
|     Mills |                    0.7 |                             4.7 |                 71.4% |
|    Keokuk |                    0.1 |                             1.4 |                 60.1% |
|    Taylor |                    0.6 |                             9.3 |                 57.1% |
|    Shelby |                    0.3 |                             2.5 |                 50.1% |
|   Webster |                    1.6 |                             4.4 |                 50.0% |
|  Buchanan |                    1.3 |                             6.1 |                 45.5% |
|    Jasper |                    0.6 |                             1.5 |                 37.4% |
|    Monroe |                    0.6 |                             7.4 |                 37.4% |
| Chickasaw |                    0.3 |                             2.4 |                 28.6% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Page |                    0.0 |                             0.0 |               \-58.8% |
|      Plymouth |                  \-0.1 |                           \-0.6 |               \-53.9% |
|    Des Moines |                    0.9 |                             2.2 |               \-50.0% |
|         Emmet |                    0.0 |                             0.0 |               \-46.1% |
|       Clinton |                    0.6 |                             1.2 |               \-45.0% |
| Pottawattamie |                    2.0 |                             2.1 |               \-43.2% |
|      Franklin |                    0.1 |                             1.4 |               \-42.8% |
|        Dallas |                    1.9 |                             2.0 |               \-41.2% |
|        Bremer |                    0.4 |                             1.7 |               \-41.2% |
|           Lee |                    1.3 |                             3.8 |               \-38.4% |
