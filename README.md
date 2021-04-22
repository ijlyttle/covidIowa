Compiled at 2021-04-22 20:19:37 UTC

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

## Tables as of 2021-04-22

As of 2021-04-22, IPDH is reporting 497 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-22 |                  447.7 |                            14.2 |                \-6.5% |
| 2021-04-21 |                  453.6 |                            14.4 |                \-8.7% |
| 2021-04-20 |                  457.0 |                            14.5 |               \-10.7% |
| 2021-04-19 |                  442.1 |                            14.0 |               \-15.1% |
| 2021-04-18 |                  439.0 |                            13.9 |               \-15.8% |
| 2021-04-17 |                  399.9 |                            12.7 |               \-23.2% |
| 2021-04-16 |                  487.9 |                            15.5 |                \-4.7% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   80.4 |                            16.4 |                  0.9% |
|          Linn |                   25.3 |                            11.2 |                  0.5% |
|         Scott |                   51.4 |                            29.7 |                \-9.4% |
|       Johnson |                   30.6 |                            20.2 |                  7.8% |
|    Black Hawk |                   15.1 |                            11.5 |                  0.9% |
|      Woodbury |                   14.3 |                            13.9 |               \-34.4% |
|       Dubuque |                   14.6 |                            15.0 |               \-31.9% |
|         Story |                   12.1 |                            12.5 |                  2.2% |
|        Dallas |                   11.1 |                            11.9 |               \-15.0% |
| Pottawattamie |                   19.6 |                            21.0 |               \-17.7% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Osceola |                    3.3 |                            55.2 |                  3.5% |
|      Emmet |                    2.9 |                            31.0 |               \-10.0% |
|  Dickinson |                    5.1 |                            29.8 |               \-10.4% |
|      Scott |                   51.4 |                            29.7 |                \-9.4% |
|       Clay |                    4.7 |                            29.4 |                 17.6% |
|        Sac |                    2.9 |                            29.4 |                 28.6% |
|     Shelby |                    3.0 |                            26.2 |                  0.0% |
|     Hardin |                    4.0 |                            23.7 |                 45.8% |
|     Warren |                   12.1 |                            23.6 |                  9.5% |
| Pocahontas |                    1.4 |                            21.6 |                 88.9% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|  Jefferson |                    1.1 |                             6.2 |                150.1% |
|      Lucas |                    1.3 |                            15.0 |                100.0% |
| Pocahontas |                    1.4 |                            21.6 |                 88.9% |
|    Fayette |                    1.3 |                             6.5 |                 60.0% |
|    Calhoun |                    0.6 |                             5.9 |                 57.1% |
|  Winnebago |                    2.0 |                            19.3 |                 50.0% |
|     Hardin |                    4.0 |                            23.7 |                 45.8% |
|    Madison |                    3.3 |                            20.1 |                 42.9% |
|     Bremer |                    1.9 |                             7.4 |                 42.8% |
|   Franklin |                    1.1 |                            11.4 |                 36.4% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|      Union |                  \-1.0 |                           \-8.2 |              \-100.0% |
|  Appanoose |                  \-0.1 |                           \-1.2 |               \-62.5% |
|       Page |                    0.6 |                             3.8 |               \-60.7% |
|  Van Buren |                  \-0.1 |                           \-2.0 |               \-50.0% |
|    Wapello |                    0.9 |                             2.5 |               \-45.8% |
|    Fremont |                    0.6 |                             8.2 |               \-45.0% |
| Winneshiek |                    1.6 |                             7.9 |               \-43.8% |
|   Plymouth |                    3.1 |                            12.5 |               \-43.1% |
|    Webster |                    1.1 |                             3.2 |               \-42.3% |
|    Audubon |                    0.0 |                             0.0 |               \-41.7% |
