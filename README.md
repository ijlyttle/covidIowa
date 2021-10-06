Compiled at 2021-10-06 23:56:09 UTC

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

## Tables as of 2021-10-05

As of 2021-10-05, IPDH is reporting 9860 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-10-05 |                 9768.9 |                           309.6 |                301.9% |
| 2021-09-28 |                 9174.1 |                           290.8 |                462.4% |
| 2021-09-21 |                 8325.6 |                           263.9 |                766.3% |
| 2021-09-14 |                 7098.0 |                           225.0 |              1 377.2% |
| 2021-09-08 |                  818.1 |                            25.9 |                308.7% |
| 2021-09-02 |                  864.4 |                            27.4 |                372.9% |
| 2021-08-26 |                 3425.9 |                           108.6 |              1 907.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                 1600.3 |                           326.5 |                341.0% |
|          Linn |                  773.0 |                           341.0 |                314.2% |
|         Scott |                  410.0 |                           237.1 |                218.6% |
|       Johnson |                  324.7 |                           214.8 |                264.2% |
|    Black Hawk |                  301.6 |                           229.8 |                 83.5% |
|      Woodbury |                  370.0 |                           358.9 |                380.9% |
|       Dubuque |                  198.1 |                           203.6 |                364.7% |
|         Story |                  193.0 |                           198.7 |                207.2% |
|        Dallas |                  252.4 |                           270.1 |                252.0% |
| Pottawattamie |                  274.3 |                           294.3 |                201.1% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Washington |                  117.3 |                           534.0 |                491.4% |
|    Calhoun |                   49.0 |                           506.8 |                483.4% |
|     Hardin |                   83.1 |                           493.5 |                378.9% |
| Des Moines |                  184.9 |                           474.4 |                212.0% |
|        Lee |                  155.6 |                           462.2 |                 96.1% |
|      Adams |                   16.4 |                           456.1 |                351.9% |
|     Greene |                   40.3 |                           453.3 |                466.6% |
|     Monroe |                   34.6 |                           448.6 |                361.1% |
|       Clay |                   71.7 |                           447.8 |              1 083.7% |
|  Appanoose |                   55.6 |                           447.2 |                661.5% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Montgomery |                   40.3 |                           406.2 |              1 213.6% |
|       Clay |                   71.7 |                           447.8 |              1 083.7% |
|   Mitchell |                   40.9 |                           386.0 |                910.3% |
|      Union |                   36.3 |                           296.4 |                866.7% |
|      Emmet |                   31.0 |                           336.7 |                729.7% |
|  Dickinson |                   52.6 |                           304.6 |                697.9% |
| Pocahontas |                   26.1 |                           395.0 |                691.6% |
|       Lyon |                   34.4 |                           292.9 |                675.1% |
|  Appanoose |                   55.6 |                           447.2 |                661.5% |
|  Poweshiek |                   55.4 |                           299.6 |                593.0% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|     Butler |                   29.6 |                           204.8 |                 69.8% |
| Black Hawk |                  301.6 |                           229.8 |                 83.5% |
|        Lee |                  155.6 |                           462.2 |                 96.1% |
|   Ringgold |                    8.9 |                           181.0 |                109.1% |
|        Ida |                   22.0 |                           320.7 |                117.6% |
|    Webster |                  145.7 |                           405.8 |                131.3% |
|      Davis |                   26.6 |                           295.2 |                132.5% |
|   Hamilton |                   41.0 |                           277.5 |                133.3% |
|   Crawford |                   65.6 |                           389.8 |                146.6% |
|   Delaware |                   39.9 |                           234.3 |                155.4% |
