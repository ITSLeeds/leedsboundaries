
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

There are various ways to break-up cities into divisions, which can be
useful for visualisation or increasing responsiveness in software such
as abstreet. There are many ways to divide-up cities, the simplest being
to use existing boundaries, that we will try in this case:

![](README_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

Let’s filter-out those based near Leeds:

![](README_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

There are 5 main areas that have a substantial chunk in Leeds:

    #> Warning in st_buffer.sfc(st_geometry(x), dist, nQuadSegs, endCapStyle =
    #> endCapStyle, : st_buffer does not correctly buffer longitude/latitude data
    #> Warning: attribute variables are assumed to be spatially constant throughout all
    #> geometries

![](README_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

    #> [1] "Leeds Central"    "Leeds East"       "Leeds North East" "Leeds North West"
    #> [5] "Leeds West"

I’ll edit them manually, combining Leeds North East and Leeds North
West:

![](README_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-14-2.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-14-3.png)<!-- -->

Alltogether, these are:

![](README_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->
