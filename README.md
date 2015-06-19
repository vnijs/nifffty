<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- [![Build Status](https://travis-ci.org/hrbrmstr/nifffty.svg)](https://travis-ci.org/hrbrmstr/nifffty) 
![Project Status: Concept - Minimal or no implementation has been done yet.](http://www.repostatus.org/badges/0.1.0/concept.svg)](http://www.repostatus.org/#concept)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/nifffty)](http://cran.r-project.org/web/packages/nifffty) 
![downloads](http://cranlogs.r-pkg.org/badges/grand-total/nifffty) -->
nifffty is a simple package to post events/data to an IFTTT Maker channel/recipe.

Inspired by a [blog post by Brian Connelly](http://bconnelly.net/2015/06/connecting-r-to-everything-with-ifttt/).

Here is a [sample public recipe](https://ifttt.com/recipes/300804-post-maker-event-values-to-dropbox-file) for posting the contents of a `maker` request to a file on Dropbox. The example below, which calls `maker("rtest", "this", "is a", "test")` will create a file in a Dropbox folder (in an `IFTTT/Maker/rtest` directory) that has the contents:

    Value 1: this
    Value 2: is a
    Value 3: test

(How the contents is formatted is entirely up to you.)

Brian's example posts an iOS notification, but you can do many, many things with this capability. Future enhancements will include the ability to *receive* Maker web request actions.

The following functions are implemented:

### News

-   Version `0.0.0.9999` released

### Installation

``` r
devtools::install_github("hrbrmstr/nifffty")
```

### Usage

``` r
library(nifffty)

# current verison
packageVersion("nifffty")
#> [1] '0.0.0.9000'
```

### Test Results

``` r
library(nifffty)
library(testthat)

date()
#> [1] "Fri Jun 19 09:32:29 2015"

maker("rtest", "this", "is a", "test")

test_dir("tests/")
#> basic functionality :
```

### Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
