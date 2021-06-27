Compiled at 2021-06-27 20:14:19 UTC

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

## Tables as of 2021-06-27

As of 2021-06-27, IPDH is reporting 54 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |
| 2021-06-21 |                   70.4 |                             2.2 |               \-14.2% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    6.0 |                             1.2 |               \-43.7% |
|          Linn |                    6.6 |                             2.9 |                 10.4% |
|         Scott |                    1.6 |                             0.9 |               \-37.9% |
|       Johnson |                    1.7 |                             1.1 |               \-20.9% |
|    Black Hawk |                   14.4 |                            11.0 |                  8.0% |
|      Woodbury |                    0.9 |                             0.8 |               \-35.0% |
|       Dubuque |                    2.4 |                             2.5 |                 14.3% |
|         Story |                    1.3 |                             1.3 |                 14.3% |
|        Dallas |                    1.1 |                             1.2 |                 25.0% |
| Pottawattamie |                    1.0 |                             1.1 |               \-33.3% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Adams |                    0.4 |                            11.9 |                 42.9% |
|     Monona |                    1.0 |                            11.6 |                100.0% |
| Black Hawk |                   14.4 |                            11.0 |                  8.0% |
|    Webster |                    3.6 |                             9.9 |                 77.8% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|     Keokuk |                    0.7 |                             7.0 |                 19.9% |
|     Benton |                    1.6 |                             6.1 |                \-5.3% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |
|        Lee |                    2.0 |                             5.9 |                 23.5% |
|   Cherokee |                    0.6 |                             5.1 |                 57.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|      Lyon |                    1.0 |                             8.5 |                100.0% |
|    Monona |                    1.0 |                            11.6 |                100.0% |
|   Webster |                    3.6 |                             9.9 |                 77.8% |
|  Cherokee |                    0.6 |                             5.1 |                 57.1% |
| Van Buren |                    0.3 |                             4.1 |                 50.1% |
|   Fayette |                    0.9 |                             4.4 |                 44.4% |
|    Clarke |                    0.4 |                             4.6 |                 42.9% |
|     Adair |                    0.4 |                             6.0 |                 42.9% |
|     Adams |                    0.4 |                            11.9 |                 42.9% |
|  Marshall |                    1.7 |                             4.4 |                 35.7% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Crawford |                  \-0.4 |                           \-2.6 |               \-69.3% |
|       Cedar |                  \-0.1 |                           \-0.8 |               \-50.0% |
|     Audubon |                    0.0 |                             0.0 |               \-50.0% |
| Buena Vista |                    0.1 |                             0.7 |               \-46.7% |
|    Plymouth |                  \-0.1 |                           \-0.6 |               \-45.4% |
|        Polk |                    6.0 |                             1.2 |               \-43.7% |
|    Buchanan |                    0.4 |                             2.0 |               \-41.2% |
|       Boone |                  \-0.1 |                           \-0.5 |               \-40.0% |
|       Scott |                    1.6 |                             0.9 |               \-37.9% |
|    Woodbury |                    0.9 |                             0.8 |               \-35.0% |
