
<!-- README.md is generated from README.Rmd. Please edit that file -->

# mapping

<!-- badges: start -->
<!-- badges: end -->

The goal of this article is to demonstrate how to visualise animated
traces in an interactive map with R.

You can set-up a basic animated map with `mapdeck` as follows:

``` r
library(mapdeck)
library(sf)
mapdeck(
location = c(145, -37.8)
, zoom = 10
, style = mapdeck_style("dark")
, token = Sys.getenv("MAPBOX")
) %>%
 add_trips(
   data = sf
   , animation_speed = 2000
   , trail_length = 1000
   , stroke_colour = "#FFFFFF"
)
```

![](https://user-images.githubusercontent.com/1825120/132259993-c4f39ac4-801c-4a38-8d8d-98fb05772d58.gif)
