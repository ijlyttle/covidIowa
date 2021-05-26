Compiled at 2021-05-26 17:43:13 UTC

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

## Tables as of 2021-05-26

As of 2021-05-26, IPDH is reporting 162 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-05-26 |                  154.3 |                             4.9 |               \-25.5% |
| 2021-05-25 |                  171.7 |                             5.4 |               \-22.0% |
| 2021-05-24 |                  175.6 |                             5.6 |               \-25.2% |
| 2021-05-23 |                  180.0 |                             5.7 |               \-24.0% |
| 2021-05-22 |                  183.0 |                             5.8 |               \-23.6% |
| 2021-05-21 |                  186.3 |                             5.9 |               \-26.9% |
| 2021-05-20 |                  197.3 |                             6.3 |               \-28.4% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   25.0 |                             5.1 |               \-30.5% |
|          Linn |                   11.0 |                             4.9 |               \-31.7% |
|         Scott |                   11.0 |                             6.4 |               \-38.7% |
|       Johnson |                    5.3 |                             3.5 |               \-20.0% |
|    Black Hawk |                    7.3 |                             5.6 |                \-1.7% |
|      Woodbury |                    4.0 |                             3.9 |               \-23.9% |
|       Dubuque |                    6.4 |                             6.6 |                 18.2% |
|         Story |                    5.1 |                             5.3 |                \-2.3% |
|        Dallas |                    4.4 |                             4.7 |               \-17.4% |
| Pottawattamie |                    2.9 |                             3.1 |               \-54.2% |

Most positive-cases, per-capita:

|      county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ----------: | ---------------------: | ------------------------------: | --------------------: |
| Cerro Gordo |                    7.0 |                            16.5 |                  1.8% |
|     Audubon |                    0.7 |                            13.0 |                 33.3% |
|     Madison |                    1.9 |                            11.4 |                 33.3% |
|     Hancock |                    1.1 |                            10.8 |                \-6.3% |
|    Franklin |                    1.0 |                             9.9 |               \-46.1% |
|       Boone |                    2.6 |                             9.8 |                 13.6% |
|         Lee |                    3.3 |                             9.8 |                 76.5% |
|  Des Moines |                    3.6 |                             9.2 |               \-49.2% |
|     Jackson |                    1.7 |                             8.8 |               \-17.4% |
|  Washington |                    1.9 |                             8.5 |                185.7% |

Most growth in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Washington |                    1.9 |                             8.5 |                185.7% |
|      Union |                    0.9 |                             7.0 |                 85.7% |
|        Lee |                    3.3 |                             9.8 |                 76.5% |
|  Allamakee |                    1.0 |                             7.3 |                 55.5% |
|    Clayton |                    1.1 |                             6.5 |                 50.0% |
|       Page |                    0.9 |                             5.7 |                 44.4% |
|    Decatur |                    0.4 |                             5.5 |                 42.9% |
| Pocahontas |                    0.4 |                             6.5 |                 42.9% |
|    O’Brien |                    0.6 |                             4.2 |                 37.4% |
|    Madison |                    1.9 |                            11.4 |                 33.3% |

Biggest decline in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Muscatine |                    2.0 |                             4.7 |               \-66.7% |
|        Bremer |                    0.4 |                             1.7 |               \-60.0% |
| Pottawattamie |                    2.9 |                             3.1 |               \-54.2% |
|     Palo Alto |                    0.0 |                             0.0 |               \-53.3% |
|        Shelby |                  \-0.3 |                           \-2.5 |               \-50.0% |
|    Des Moines |                    3.6 |                             9.2 |               \-49.2% |
|      Franklin |                    1.0 |                             9.9 |               \-46.1% |
|      Cherokee |                  \-0.1 |                           \-1.3 |               \-45.4% |
|     Van Buren |                  \-0.1 |                           \-2.0 |               \-45.4% |
|          Cass |                    0.1 |                             1.1 |               \-42.8% |
