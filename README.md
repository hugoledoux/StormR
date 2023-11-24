

# StormR R package <img src="man/figures/logo.png" align="right" alt="" width="120" />

<!-- badges: start -->
[![codecov](https://codecov.io/github/umr-amap/StormR/branch/master/graph/badge.svg?token=5YMVL4TFB5)](https://app.codecov.io/github/umr-amap/StormR)
[![SWH](https://archive.softwareheritage.org/badge/origin/https://github.com/umr-amap/StormR/)](https://archive.softwareheritage.org/browse/origin/?origin_url=https://github.com/umr-amap/StormR)
<!-- badges: end -->

## Overview

`StormR` is an R package allowing to easily extract storm track data for given locations or areas of interests, to generate wind speed and direction fields, and to compute summary statistics characterising the behaviour of winds generated by tropical storms and cyclones: maximum sustained wind speed, power dissipation index, and duration of exposure to winds reaching defined speed thresholds.

## Usage

### Installing StormR

`StormR` is now [available on CRAN](https://cran.r-project.org/web/packages/StormR/index.html) on version `0.1.1`.
You can install it as follows:

``` r
install.packages("StormR")
```

The latest development version can be installed from GitHub as follows,

``` r
#install.packages("devtools")
devtools::install_github("umr-amap/StormR")
```

### Loading StormR package

``` r
library(StormR)
```

## Main functions

| **Name** | **Description** | **Inputs** | **Outputs** |
|:--:|:----:|:-----------:|:-----:|
|`defStormsDataset()`|Creates a `stormsDataset` object|".nc" (NetCDF) file|`stormsDataset` object|
|`defStormsList()`|Extracts storms|`stormsDataset` object|`StormsList` object|
|`plotStorms()`|Plots storms track data|`StormsList` object||
|`temporalBehaviour()`|Computes wind speed, direction time series, and summary statistics for a given set of point coordinates |`StormsList` object|lists of data.frame objects|
|`spatialBehaviour()`|Computes 2D wind fields and summary statistics over a given location of interest |`StormsList` object|`SpatRaster` object|
|`plotBehaviour()`|Plots 2D wind fields and summary statistics|`StormsList` + `SpatRaster` objects||
|`writeRast()`|Exports wind fields and summary statistics to file|`SpatRaster` object|`.tiff` or `.nc` file|

## Contributing
You are welcome to contribute to the `StormR` package. Just fork the project and create a pull request with your changes and we will review it as soon as possible.

## Reporting issues
Issues can be reported [here](https://github.com/umr-amap/StormR/issues/new/choose). Simply choose the appropriate template and fill in the requested information.

## Seeking help
If you need help with the `StormR` package, please open a new discussion on the [Q&A section on github](https://github.com/umr-amap/StormR/discussions/categories/q-a). We will do our best to answer your questions. Other users are also welcome to help you.

## Funding
This work was supported by Hermon Slade Foundation, [grant HSF 19105](http://www.hermonslade.org.au/hsf-19105/).
