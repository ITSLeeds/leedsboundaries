
<!-- README.md is generated from README.Rmd. Please edit that file -->

# leedsboundaries

<!-- badges: start -->
<!-- badges: end -->

The goal of leedsboundaries is to show different ways of defining the
geographic extent of ‘Leeds’ in a reproducible way. Leeds is a city and
local authority in the North of England, North of Sheffield, South of
Newcastle, East of Manchester and West of Hull.

<!-- To reproduce this document you must have a recent version of R and the following packages loaded: -->

It is most easily defined by its local authority boundaries, which are
as follows:

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

For the purposes of transport planning and other applications, other
definitions are useful.

One way of defining Leeds is everything in ring roads. This looks
roughly as follows:

![](README_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

A neater boundary can be obtained by taking the ‘concave hull’ of major
roads in the rough outline shown above:

![](README_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

A simplified version of the previous polygon is as follows:

![](README_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

The resulting file is saved as `sub_area_simple.geojson` in this repo.
