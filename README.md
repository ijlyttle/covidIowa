Compiled at 2021-02-28 21:13:43 UTC

<!-- README.md is generated from README.Rmd. Please edit that file -->

# covidIowa

<!-- badges: start -->
<!-- badges: end -->

The goal of this repository is to give a county-level summary of
COVID-19 cases in Iowa. The data is taken from a series of daily
snapshots of the [accessibility
page](https://coronavirus.iowa.gov/pages/access) provided by the Iowa
Department of Public Health.

I don’t know if, in this case, **cases** means positive individuals or
positive tests. All I know is that small numbers are good and big
numbers are bad.

If you want to work with the data yourself, it’s available here:

-   [`iowa_county_meta.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_meta.csv):
    county metadata, things like estimated 2019 population from
    [ICIP](https://www.icip.iastate.edu/tables/population/counties-estimates)
    at Iowa State University.
-   [`iowa_county_data.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    daily numbers by county from IDPH, going back to 2020-05-25.
-   [`iowa_county_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    In addition to county metadata, total cases (and per 100k), one week
    averages of new cases (and per 100k), and week-over-week change in
    cases (as a ratio).
-   [`iowa_cases_week.csv`](https://github.com/ijlyttle/covidIowa/blob/master/workflow/data/99-publish/iowa_county_data.csv):
    Similar to `iowa_county_cases_week.csv`, but aggregated for the
    entire state.

## Plots

![](workflow/data/99-publish/iowa_cases.png)

![](workflow/data/99-publish/iowa_change.png)

## Tables as of 2021-02-28

For the entire state, over the past week:

|       date | daily new cases | daily new cases per 100k | week-over-week change |
|-----------:|----------------:|-------------------------:|----------------------:|
| 2021-02-28 |           534.0 |                     16.9 |                 7.60% |
| 2021-02-27 |           540.1 |                     17.1 |                 6.70% |
| 2021-02-26 |           540.4 |                     17.1 |                 4.20% |
| 2021-02-25 |           527.7 |                     16.7 |                -3.00% |
| 2021-02-24 |           524.0 |                     16.6 |                -8.80% |
| 2021-02-23 |           510.1 |                     16.2 |               -19.40% |
| 2021-02-22 |           494.0 |                     15.7 |               -25.40% |

For the most-populated counties:

|        county | daily new cases | daily new cases per 100k | week-over-week change |
|--------------:|----------------:|-------------------------:|----------------------:|
|          Polk |           107.4 |                     21.9 |                -1.30% |
|          Linn |            21.9 |                      9.6 |                -2.40% |
|         Scott |            21.0 |                     12.1 |                -3.70% |
|       Johnson |            18.1 |                     12.0 |                 2.30% |
|    Black Hawk |            13.7 |                     10.5 |                15.70% |
|      Woodbury |            18.6 |                     18.0 |                 3.80% |
|       Dubuque |            19.1 |                     19.7 |                18.50% |
|         Story |            18.7 |                     19.3 |                10.40% |
|        Dallas |            25.3 |                     27.1 |                16.50% |
| Pottawattamie |            14.7 |                     15.8 |                10.00% |

Most cases reported, per-capita:

|      county | daily new cases | daily new cases per 100k | week-over-week change |
|------------:|----------------:|-------------------------:|----------------------:|
|      Jasper |            18.0 |                     48.4 |               -16.90% |
|     Wapello |            14.9 |                     42.5 |                22.00% |
|        Page |             5.9 |                     38.8 |               -56.00% |
| Buena Vista |             6.6 |                     33.5 |               103.90% |
|    Crawford |             4.9 |                     28.9 |                24.20% |
|       Cedar |             5.3 |                     28.4 |                18.90% |
|      Dallas |            25.3 |                     27.1 |                16.50% |
|      Benton |             6.9 |                     26.7 |                -5.20% |
|     Osceola |             1.6 |                     26.4 |                28.60% |
|      Clarke |             2.4 |                     25.9 |               -17.20% |

Most growth in cases, week-over-week:

|      county | daily new cases | daily new cases per 100k | week-over-week change |
|------------:|----------------:|-------------------------:|----------------------:|
| Buena Vista |             6.6 |                     33.5 |               103.90% |
|    Harrison |             2.4 |                     17.3 |                71.40% |
|        Tama |             3.4 |                     20.3 |                63.20% |
|      Bremer |             5.3 |                     21.1 |                63.00% |
|       Mills |             2.0 |                     13.2 |                61.60% |
|      Hardin |             3.6 |                     21.2 |                60.00% |
|       Floyd |             1.0 |                      6.4 |                55.50% |
|   Jefferson |             1.6 |                      8.6 |                50.00% |
|  Pocahontas |             0.4 |                      6.5 |                42.90% |
|     O’Brien |             2.7 |                     19.7 |                36.80% |

Biggest decline in cases, week-over-week:

|     county | daily new cases | daily new cases per 100k | week-over-week change |
|-----------:|----------------:|-------------------------:|----------------------:|
| Washington |             1.3 |                      5.9 |               -61.00% |
|      Adair |             1.6 |                     22.0 |               -57.20% |
|       Page |             5.9 |                     38.8 |               -56.00% |
|     Taylor |             0.3 |                      4.7 |               -43.70% |
|   Cherokee |             0.7 |                      6.4 |               -42.90% |
|   Hamilton |             1.4 |                      9.7 |               -41.40% |
|       Clay |             0.9 |                      5.4 |               -40.90% |
|   Marshall |             4.1 |                     10.5 |               -37.90% |
|     Howard |             1.1 |                     12.5 |               -37.50% |
|    Audubon |             0.7 |                     13.0 |               -36.80% |
