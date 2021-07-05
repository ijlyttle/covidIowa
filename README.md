Compiled at 2021-07-05 20:15:16 UTC

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

## Tables as of 2021-07-05

As of 2021-07-05, IPDH is reporting 23 new cases since the previous day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-07-05 |                   83.6 |                             2.6 |                 20.8% |
| 2021-07-04 |                   86.0 |                             2.7 |                 26.9% |
| 2021-07-03 |                   85.0 |                             2.7 |                 24.6% |
| 2021-07-02 |                   85.3 |                             2.7 |                 24.8% |
| 2021-07-01 |                   81.4 |                             2.6 |                 19.0% |
| 2021-06-30 |                   73.3 |                             2.3 |                  4.6% |
| 2021-06-29 |                   72.3 |                             2.3 |               \-10.0% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   10.7 |                             2.2 |                 64.0% |
|          Linn |                    4.3 |                             1.9 |               \-28.8% |
|         Scott |                    2.6 |                             1.5 |                 25.0% |
|       Johnson |                    1.6 |                             1.0 |                \-5.3% |
|    Black Hawk |                   12.4 |                             9.5 |               \-13.8% |
|      Woodbury |                    2.4 |                             2.4 |                100.1% |
|       Dubuque |                    1.7 |                             1.8 |               \-20.9% |
|         Story |                    1.1 |                             1.2 |                 36.4% |
|        Dallas |                    1.3 |                             1.4 |                 33.4% |
| Pottawattamie |                    1.6 |                             1.7 |                 12.5% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Wayne |                    1.0 |                            15.5 |                100.0% |
|   Humboldt |                    1.4 |                            15.0 |                112.5% |
|    Webster |                    5.1 |                            14.3 |                 38.7% |
| Black Hawk |                   12.4 |                             9.5 |               \-13.8% |
|   Ringgold |                    0.4 |                             8.8 |                 42.9% |
|        Lee |                    2.9 |                             8.5 |                 42.1% |
|      Adams |                    0.3 |                             7.9 |               \-10.0% |
|    Calhoun |                    0.7 |                             7.4 |                 50.0% |
|   Franklin |                    0.7 |                             7.1 |                 50.0% |
| Winneshiek |                    1.3 |                             6.4 |                  0.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Humboldt |                    1.4 |                            15.0 |                112.5% |
|    Woodbury |                    2.4 |                             2.4 |                100.1% |
| Buena Vista |                    0.7 |                             3.6 |                100.0% |
|       Wayne |                    1.0 |                            15.5 |                100.0% |
|      Warren |                    1.7 |                             3.3 |                 72.8% |
|   Dickinson |                    0.7 |                             4.1 |                 71.4% |
|     Carroll |                    0.4 |                             2.1 |                 66.7% |
|        Polk |                   10.7 |                             2.2 |                 64.0% |
|    Plymouth |                    0.6 |                             2.3 |                 57.1% |
|      Jasper |                    1.0 |                             2.7 |                 55.5% |

Biggest decline in positive cases, week-over-week:

|   county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| -------: | ---------------------: | ------------------------------: | --------------------: |
|   Monona |                    0.0 |                             0.0 |               \-50.0% |
| Marshall |                    1.0 |                             2.5 |               \-33.3% |
| Buchanan |                    0.0 |                             0.0 |               \-30.0% |
|    Adair |                    0.0 |                             0.0 |               \-30.0% |
|     Linn |                    4.3 |                             1.9 |               \-28.8% |
|   Keokuk |                    0.1 |                             1.4 |               \-27.2% |
|  O’Brien |                  \-0.1 |                           \-1.0 |               \-25.0% |
|   Wright |                    0.3 |                             2.3 |               \-25.0% |
|    Henry |                    0.6 |                             2.9 |               \-21.5% |
|     Lyon |                    0.6 |                             4.9 |               \-21.5% |
