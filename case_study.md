case study
================
Lu Qiu
2023-10-10

``` r
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.3     ✔ readr     2.1.4
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.0
    ## ✔ ggplot2   3.4.3     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.0
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

### Get the data

``` r
library(p8105.datasets)
data(nyc_airbnb)
```

``` r
nyc_airbnb =
  nyc_airbnb |>
  rename(borough = neighbourhood_group) |>
  mutate(stars = review_scores_location / 2)
```

## Brainstorm questions

- Where are AirBNBs expensive?
  - Borough? Neighborhood?
  - Do other factors affect price? What about rating?
- Are AirBNBs illegal and do they get shut down?
- Which units have the most availability?
- How is review score impacted by location?
- How many apts are run by one host?
- 
