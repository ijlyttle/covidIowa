Compiled at 2021-08-24 23:53:46 UTC

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

## Tables as of 2021-08-19

As of 2021-08-19, IPDH is reporting 5697 new cases since the previous
day.

For the entire state, over the past week:

|       date | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| 2021-08-19 |                 2430.0 |                            77.0 |              1 431.7% |
| 2021-08-12 |                 1630.6 |                            51.7 |                942.1% |
| 2021-08-04 |                  960.1 |                            30.4 |                534.7% |
| 2021-07-28 |                  479.6 |                            15.2 |                241.9% |
| 2021-07-21 |                  199.4 |                             6.3 |                 51.3% |
| 2021-07-20 |                  182.0 |                             5.8 |                 54.3% |
| 2021-07-19 |                  169.7 |                             5.4 |                 65.5% |

For the most-populated counties:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Polk |                  362.1 |                            73.9 |              1 782.9% |
|          Linn |                  185.9 |                            82.0 |              3 014.3% |
|         Scott |                  128.0 |                            74.0 |              1 380.4% |
|       Johnson |                   88.4 |                            58.5 |              1 152.0% |
|    Black Hawk |                  163.9 |                           124.9 |                767.7% |
|      Woodbury |                   76.1 |                            73.8 |                958.8% |
|       Dubuque |                   41.9 |                            43.0 |              1 479.1% |
|         Story |                   62.1 |                            64.0 |              1 200.0% |
|        Dallas |                   71.0 |                            76.0 |              1 475.1% |
| Pottawattamie |                   90.4 |                            97.0 |              1 782.4% |

Most positive-cases, per-capita:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
|        Lee |                   78.9 |                           234.3 |              2 050.2% |
|    Webster |                   62.4 |                           173.9 |                455.0% |
|   Crawford |                   26.0 |                           154.6 |              1 159.9% |
| Des Moines |                   58.6 |                           150.3 |                942.5% |
|        Ida |                    9.6 |                           139.5 |                824.8% |
| Black Hawk |                  163.9 |                           124.9 |                767.7% |
|     Wright |                   15.3 |                           121.7 |                356.1% |
|      Davis |                   10.9 |                           120.6 |                937.4% |
|   Franklin |                   12.0 |                           119.2 |                313.6% |
|     Butler |                   17.0 |                           117.7 |              1 045.8% |

Most growth in positive cases, week-over-week:

|        county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ------------: | ---------------------: | ------------------------------: | --------------------: |
|          Linn |                  185.9 |                            82.0 |              3 014.3% |
|           Lee |                   78.9 |                           234.3 |              2 050.2% |
|      Marshall |                   32.1 |                            81.6 |              1 833.7% |
|          Polk |                  362.1 |                            73.9 |              1 782.9% |
| Pottawattamie |                   90.4 |                            97.0 |              1 782.4% |
|       Fayette |                   15.9 |                            80.7 |              1 585.7% |
|       Dubuque |                   41.9 |                            43.0 |              1 479.1% |
|        Dallas |                   71.0 |                            76.0 |              1 475.1% |
|         Scott |                  128.0 |                            74.0 |              1 380.4% |
|         Henry |                   19.7 |                            98.8 |              1 349.5% |

Biggest decline in positive cases, week-over-week:

|     county | daily pos. (week avg.) | daily pos. per 100k (week avg.) | week-over-week change |
| ---------: | ---------------------: | ------------------------------: | --------------------: |
| Montgomery |                    2.1 |                            21.6 |                 29.4% |
|      Adair |                    3.3 |                            45.9 |                100.0% |
|     Monroe |                    6.7 |                            87.1 |                116.0% |
|    Calhoun |                    7.6 |                            78.3 |                122.2% |
|      Adams |                    2.9 |                            79.3 |                145.5% |
|    Decatur |                    4.9 |                            61.7 |                156.2% |
|       Cass |                    6.9 |                            53.4 |                161.9% |
| Pocahontas |                    2.4 |                            36.7 |                166.6% |
|     Monona |                    3.9 |                            44.8 |                183.4% |
|     Taylor |                    1.9 |                            30.3 |                185.7% |
