Compiled at 2021-07-01 20:17:26 UTC

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

## Tables as of 2021-07-01

As of 2021-07-01, IPDH is reporting 119 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |
| 2021-06-28 |                   69.0 |                             2.2 |                \-2.0% |
| 2021-06-27 |                   67.6 |                             2.1 |               \-10.4% |
| 2021-06-26 |                   68.0 |                             2.2 |                \-9.6% |
| 2021-06-25 |                   68.1 |                             2.2 |               \-16.8% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                    7.6 |                             1.5 |               \-10.4% |
|          Linn |                    4.7 |                             2.1 |               \-25.9% |
|         Scott |                    2.7 |                             1.6 |                 44.5% |
|       Johnson |                    2.9 |                             1.9 |                 68.7% |
|    Black Hawk |                   14.3 |                            10.9 |                  0.9% |
|      Woodbury |                    1.6 |                             1.5 |                 50.0% |
|       Dubuque |                    2.0 |                             2.1 |                \-4.5% |
|         Story |                    1.3 |                             1.3 |                 33.4% |
|        Dallas |                    1.0 |                             1.1 |                \-6.7% |
| Pottawattamie |                    1.3 |                             1.4 |               \-15.8% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Webster |                    4.7 |                            13.1 |                 81.8% |
|   Humboldt |                    1.1 |                            12.0 |                114.3% |
|      Adams |                    0.4 |                            11.9 |                 25.0% |
|      Wayne |                    0.7 |                            11.1 |                 71.4% |
| Black Hawk |                   14.3 |                            10.9 |                  0.9% |
|        Lee |                    3.6 |                            10.6 |                191.0% |
| Winneshiek |                    1.9 |                             9.3 |                 42.8% |
|    Audubon |                    0.4 |                             7.8 |                100.1% |
|       Lyon |                    0.9 |                             7.3 |                  8.3% |
|    Decatur |                    0.6 |                             7.3 |                 57.1% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|       Lee |                    3.6 |                            10.6 |                191.0% |
|  Humboldt |                    1.1 |                            12.0 |                114.3% |
|   Audubon |                    0.4 |                             7.8 |                100.1% |
|   Webster |                    4.7 |                            13.1 |                 81.8% |
|     Wayne |                    0.7 |                            11.1 |                 71.4% |
|    Warren |                    1.4 |                             2.8 |                 70.0% |
|   Johnson |                    2.9 |                             1.9 |                 68.7% |
|    Hardin |                    1.1 |                             6.8 |                 66.6% |
| Muscatine |                    1.3 |                             3.0 |                 60.0% |
|  Crawford |                    0.6 |                             3.4 |                 57.1% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monona |                  \-0.1 |                           \-1.7 |               \-60.0% |
| Marshall |                    0.6 |                             1.4 |               \-50.0% |
|    Sioux |                    0.1 |                             0.4 |               \-46.7% |
|    Henry |                    0.1 |                             0.7 |               \-42.8% |
| Buchanan |                    0.1 |                             0.7 |               \-38.4% |
|    Adair |                    0.0 |                             0.0 |               \-30.0% |
|  Mahaska |                    0.1 |                             0.6 |               \-27.2% |
|     Linn |                    4.7 |                             2.1 |               \-25.9% |
|    Boone |                    0.0 |                             0.0 |               \-22.2% |
| Delaware |                    0.0 |                             0.0 |               \-22.2% |
