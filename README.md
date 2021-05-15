Compiled at 2021-05-15 17:11:47 UTC

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

## Tables as of 2021-05-15

As of 2021-05-15, IPDH is reporting 193 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-15 |                  239.9 |                             7.6 |               \-29.2% |
| 2021-05-14 |                  255.1 |                             8.1 |               \-27.4% |
| 2021-05-13 |                  275.9 |                             8.7 |               \-20.7% |
| 2021-05-12 |                  333.9 |                            10.6 |                  6.1% |
| 2021-05-11 |                  300.1 |                             9.5 |               \-18.1% |
| 2021-05-10 |                  310.7 |                             9.8 |               \-14.3% |
| 2021-05-09 |                  315.0 |                            10.0 |               \-14.9% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   40.3 |                             8.2 |               \-34.3% |
|          Linn |                   17.0 |                             7.5 |               \-24.1% |
|         Scott |                   25.3 |                            14.6 |               \-34.0% |
|       Johnson |                    7.6 |                             5.0 |               \-34.1% |
|    Black Hawk |                    7.4 |                             5.7 |                \-7.8% |
|      Woodbury |                    5.0 |                             4.8 |               \-22.2% |
|       Dubuque |                    4.9 |                             5.0 |               \-34.9% |
|         Story |                    6.9 |                             7.1 |               \-36.8% |
|        Dallas |                    7.0 |                             7.5 |               \-32.5% |
| Pottawattamie |                    9.0 |                             9.7 |               \-27.1% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|    Franklin |                    4.3 |                            42.6 |                 27.6% |
|     Hancock |                    2.0 |                            18.8 |                 16.7% |
|  Des Moines |                    7.3 |                            18.7 |                 38.1% |
|   Muscatine |                    7.7 |                            18.1 |               \-14.1% |
|     Osceola |                    1.0 |                            16.8 |                 27.3% |
|     Calhoun |                    1.6 |                            16.2 |               \-40.0% |
|   Winnebago |                    1.6 |                            15.2 |                \-5.3% |
|       Scott |                   25.3 |                            14.6 |               \-34.0% |
| Cerro Gordo |                    5.3 |                            12.5 |                  4.8% |
|       Jones |                    2.4 |                            11.7 |                \-4.0% |

Most growth in positive cases, week-over-week:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
|         Ida |                    0.4 |                             6.3 |                 66.7% |
|    Hamilton |                    1.1 |                             7.7 |                 50.0% |
|  Pocahontas |                    0.4 |                             6.5 |                 42.9% |
| Buena Vista |                    1.0 |                             5.1 |                 40.0% |
|  Des Moines |                    7.3 |                            18.7 |                 38.1% |
|    Buchanan |                    1.3 |                             6.1 |                 33.4% |
|    Cherokee |                    0.7 |                             6.4 |                 33.3% |
|    Mitchell |                    0.9 |                             8.1 |                 30.0% |
|   Van Buren |                    0.3 |                             4.1 |                 28.6% |
|    Franklin |                    4.3 |                            42.6 |                 27.6% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|   Crawford |                    0.4 |                             2.6 |               \-64.3% |
| Washington |                    0.6 |                             2.6 |               \-60.7% |
|     Jasper |                    2.6 |                             6.9 |               \-58.3% |
|    Madison |                    1.9 |                            11.4 |               \-57.4% |
|      Union |                    0.3 |                             2.3 |               \-57.1% |
|      Emmet |                    0.4 |                             4.7 |               \-54.5% |
|      Sioux |                    1.6 |                             4.5 |               \-52.6% |
|    Decatur |                    0.3 |                             3.6 |               \-47.1% |
| Montgomery |                    0.1 |                             1.4 |               \-46.7% |
|  Jefferson |                    0.0 |                             0.0 |               \-46.1% |
