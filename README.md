Compiled at 2021-04-08 17:13:58 UTC

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

## Tables as of 2021-04-08

As of 2021-04-08, IPDH is reporting 666 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-04-08 |                  525.1 |                            16.6 |               \-19.7% |
| 2021-04-07 |                  545.7 |                            17.3 |               \-15.8% |
| 2021-04-06 |                  595.1 |                            18.9 |                  6.2% |
| 2021-04-05 |                  522.7 |                            16.6 |                \-9.8% |
| 2021-04-04 |                  586.0 |                            18.6 |                  8.5% |
| 2021-04-03 |                  600.4 |                            19.0 |                 13.6% |
| 2021-04-02 |                  651.3 |                            20.6 |                 34.6% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                   89.4 |                            18.2 |               \-28.8% |
|          Linn |                   20.0 |                             8.8 |               \-10.9% |
|         Scott |                   60.1 |                            34.8 |               \-13.7% |
|       Johnson |                   28.4 |                            18.8 |                  4.6% |
|    Black Hawk |                   15.6 |                            11.9 |                \-3.3% |
|      Woodbury |                   22.1 |                            21.5 |               \-30.2% |
|       Dubuque |                   28.4 |                            29.2 |                 26.4% |
|         Story |                   17.7 |                            18.2 |               \-34.2% |
|        Dallas |                   12.9 |                            13.8 |               \-47.3% |
| Pottawattamie |                   27.3 |                            29.3 |                  4.2% |

Most positive-cases, per-capita:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|     Dickinson |                   11.4 |                            66.2 |               \-15.5% |
|         Emmet |                    3.7 |                            40.3 |               \-28.3% |
|      Plymouth |                    9.4 |                            37.5 |                  1.4% |
|          Clay |                    5.6 |                            34.8 |               \-41.0% |
|         Scott |                   60.1 |                            34.8 |               \-13.7% |
|         Worth |                    2.3 |                            31.0 |                155.5% |
|      Delaware |                    5.1 |                            30.2 |               \-18.9% |
| Pottawattamie |                   27.3 |                            29.3 |                  4.2% |
|       Dubuque |                   28.4 |                            29.2 |                 26.4% |
|       Carroll |                    5.7 |                            28.3 |                123.8% |

Most growth in positive cases, week-over-week:

|    county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| --------: | ---------------------: | ------------------------------: | --------------------: |
|     Worth |                    2.3 |                            31.0 |                155.5% |
|  Harrison |                    3.7 |                            26.4 |                135.7% |
|   Carroll |                    5.7 |                            28.3 |                123.8% |
|   Clayton |                    3.6 |                            20.3 |                100.0% |
|    Greene |                    1.3 |                            14.5 |                 60.0% |
|      Tama |                    1.0 |                             5.9 |                 55.5% |
|   Mahaska |                    2.9 |                            12.9 |                 42.1% |
|   Hancock |                    2.1 |                            20.2 |                 37.5% |
|    Monroe |                    1.3 |                            16.7 |                 33.4% |
| Winnebago |                    1.4 |                            13.8 |                 30.8% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|    Guthrie |                    0.7 |                             6.7 |               \-71.4% |
|        Lee |                    3.1 |                             9.3 |               \-68.1% |
|     Jasper |                    3.0 |                             8.1 |               \-66.3% |
|  Palo Alto |                    1.9 |                            20.9 |               \-53.5% |
|   Mitchell |                    0.6 |                             5.4 |               \-52.2% |
|     Shelby |                    1.4 |                            12.5 |               \-51.4% |
| Pocahontas |                    0.0 |                             0.0 |               \-50.0% |
|     Dallas |                   12.9 |                            13.8 |               \-47.3% |
|    Wapello |                    1.6 |                             4.5 |               \-47.1% |
|   Humboldt |                    0.3 |                             3.0 |               \-47.1% |
