Compiled at 2021-06-28 20:14:41 UTC

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

## Tables as of 2021-06-28

As of 2021-06-28, IPDH is reporting 40 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |
| 2021-06-24 |                   68.3 |                             2.2 |               \-18.1% |
| 2021-06-23 |                   70.0 |                             2.2 |               \-15.5% |
| 2021-06-22 |                   80.4 |                             2.5 |                 10.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    6.1 |                             1.3 |               \-39.8% |
|          Linn |                    6.4 |                             2.8 |                 15.6% |
|         Scott |                    1.9 |                             1.1 |               \-28.6% |
|       Johnson |                    1.7 |                             1.1 |                \-9.5% |
|    Black Hawk |                   14.6 |                            11.1 |                 14.7% |
|      Woodbury |                    0.7 |                             0.7 |               \-33.3% |
|       Dubuque |                    2.4 |                             2.5 |                 20.0% |
|         Story |                    0.6 |                             0.6 |               \-42.1% |
|        Dallas |                    0.7 |                             0.8 |                \-7.7% |
| Pottawattamie |                    1.3 |                             1.4 |               \-11.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Adams |                    0.4 |                            11.9 |                 42.9% |
|     Monona |                    1.0 |                            11.6 |                100.0% |
| Black Hawk |                   14.6 |                            11.1 |                 14.7% |
|    Webster |                    3.4 |                             9.6 |                 93.7% |
|       Lyon |                    1.0 |                             8.5 |                100.0% |
|    Decatur |                    0.6 |                             7.3 |                 37.4% |
| Winneshiek |                    1.3 |                             6.4 |                  6.7% |
|     Benton |                    1.6 |                             6.1 |                 12.5% |
|     Clarke |                    0.6 |                             6.1 |                 57.1% |
|      Adair |                    0.4 |                             6.0 |                 42.9% |

Most growth in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|     Lyon |                    1.0 |                             8.5 |                100.0% |
|   Monona |                    1.0 |                            11.6 |                100.0% |
|  Webster |                    3.4 |                             9.6 |                 93.7% |
| Marshall |                    2.0 |                             5.1 |                 91.0% |
|   Hardin |                    0.9 |                             5.1 |                 85.7% |
|     Iowa |                    0.4 |                             2.7 |                 66.7% |
|      Lee |                    1.7 |                             5.1 |                 58.3% |
| Cherokee |                    0.6 |                             5.1 |                 57.1% |
|   Clarke |                    0.6 |                             6.1 |                 57.1% |
|   Wright |                    0.7 |                             5.7 |                 50.0% |

Biggest decline in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Buena Vista |                  \-0.1 |                           \-0.7 |               \-64.7% |
|     Carroll |                  \-0.1 |                           \-0.7 |               \-50.0% |
|       Story |                    0.6 |                             0.6 |               \-42.1% |
|     Audubon |                    0.0 |                             0.0 |               \-41.7% |
|        Polk |                    6.1 |                             1.3 |               \-39.8% |
|    Buchanan |                    0.4 |                             2.0 |               \-37.5% |
|       Sioux |                    0.3 |                             0.8 |               \-35.7% |
|    Woodbury |                    0.7 |                             0.7 |               \-33.3% |
|     Mahaska |                    0.1 |                             0.6 |               \-33.3% |
|      Bremer |                    0.6 |                             2.3 |               \-31.3% |
