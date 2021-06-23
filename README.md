Compiled at 2021-06-23 23:52:06 UTC

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

## Tables as of 2021-06-23

As of 2021-06-23, IPDH is reporting 110 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |
| 2021-06-20 |                   75.6 |                             2.4 |                \-3.8% |
| 2021-06-19 |                   75.3 |                             2.4 |                \-7.9% |
| 2021-06-18 |                   82.1 |                             2.6 |                  3.7% |
| 2021-06-17 |                   83.6 |                             2.6 |                \-0.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    8.4 |                             1.7 |               \-23.3% |
|          Linn |                    6.7 |                             3.0 |               \-12.9% |
|         Scott |                    1.6 |                             0.9 |               \-43.8% |
|       Johnson |                    2.1 |                             1.4 |               \-12.0% |
|    Black Hawk |                   13.0 |                             9.9 |                \-7.5% |
|      Woodbury |                    0.7 |                             0.7 |               \-53.9% |
|       Dubuque |                    1.9 |                             1.9 |               \-35.5% |
|         Story |                    1.1 |                             1.2 |                 15.4% |
|        Dallas |                    0.7 |                             0.8 |               \-40.0% |
| Pottawattamie |                    1.9 |                             2.0 |                \-4.8% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Black Hawk |                   13.0 |                             9.9 |                \-7.5% |
|     Keokuk |                    1.0 |                             9.8 |                 75.0% |
|     Monona |                    0.7 |                             8.3 |                 71.4% |
|      Worth |                    0.4 |                             5.8 |                 11.1% |
|      Mills |                    0.9 |                             5.7 |                  8.3% |
|   Marshall |                    2.1 |                             5.4 |                119.9% |
|    Audubon |                    0.3 |                             5.2 |               \-25.0% |
|     Benton |                    1.3 |                             5.0 |                  0.0% |
|      Henry |                    1.0 |                             5.0 |                 75.0% |
|       Lyon |                    0.6 |                             4.9 |                 57.1% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
| Marshall |                    2.1 |                             5.4 |                119.9% |
|    Henry |                    1.0 |                             5.0 |                 75.0% |
|   Keokuk |                    1.0 |                             9.8 |                 75.0% |
|   Monona |                    0.7 |                             8.3 |                 71.4% |
| Plymouth |                    0.4 |                             1.7 |                 66.7% |
|     Lyon |                    0.6 |                             4.9 |                 57.1% |
|    Jones |                    0.4 |                             2.1 |                 42.9% |
|   Bremer |                    1.0 |                             4.0 |                 40.0% |
| Delaware |                    0.3 |                             1.7 |                 28.6% |
| Cherokee |                    0.3 |                             2.5 |                 28.6% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Woodbury |                    0.7 |                             0.7 |               \-53.9% |
| Cerro Gordo |                    0.9 |                             2.0 |               \-50.0% |
|      Warren |                    0.4 |                             0.8 |               \-47.3% |
|  Washington |                    0.0 |                             0.0 |               \-46.1% |
|       Scott |                    1.6 |                             0.9 |               \-43.8% |
|      Dallas |                    0.7 |                             0.8 |               \-40.0% |
|     Carroll |                    0.0 |                             0.0 |               \-36.3% |
|      Monroe |                    0.0 |                             0.0 |               \-36.3% |
|      Taylor |                    0.0 |                             0.0 |               \-36.3% |
| Buena Vista |                    0.3 |                             1.5 |               \-35.7% |
