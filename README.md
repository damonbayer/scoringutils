

# scoringutils: Utilities for Scoring and Assessing Predictions

[![R-CMD-check](https://github.com/epiforecasts/EpiNow/workflows/R-CMD-check/badge.svg)](https://github.com/epiforecasts/scoringutils/actions)
[![codecov](https://codecov.io/gh/epiforecasts/scoringutils/branch/master/graphs/badge.svg)](https://codecov.io/gh/epiforecasts/scoringutils/) 
[![CRAN\_Release\_Badge](https://www.r-pkg.org/badges/version-ago/scoringutils)](https://CRAN.R-project.org/package=scoringutils)
[![develVersion](https://img.shields.io/badge/devel%20version-0.1.1-green.svg?style=flat)](https://github.com/epiforecasts/scoringutils)
[![metacran
downloads](http://cranlogs.r-pkg.org/badges/grand-total/scoringutils)](https://cran.r-project.org/package=scoringutils)
<!-- badges: end -->

This package is designed to help with assessing the quality of predictions. 
It provides a collection of proper scoring rules and metrics that can be 
accessed independently or collectively to score predictions automatically. 
It provides some metrics, e.g. for evaluating bias or for 
assessing calibration using 
the probability integral transformation that go beyond the scope of existing
packages like `scoringRules`. Through the function `eval_forecasts` it also 
provides functionality that automatically and very conveniently
scores forecasts using `data.table`. 

For a quick overview, have a look at the [package vignette](https://cran.rstudio.com/web/packages/scoringutils/vignettes/scoringutils.html)

Predicitions can be either probabilistic forecasts (generally predictive 
samples generated by Markov Chain Monte Carlo procedures), quantile
forecasts or point forecasts. 
The type of the predictions and the true values can be either continuous, 
integer, or binary. 

## Installation

Install the stable version from CRAN using 
``` r
install.packages("scoringutils")
```

New features not yet available on CRAN be accessed via
[`{drat}`](https://epiforecasts.io/drat/):

```r
install.packages("drat")
drat:::add("epiforecasts")
install.packages("scoringutils")
```

The version of the package under active development can also be installed with: 

```r
remotes::install_github("epiforecasts/scoringutils")
```

## Supported scores and metrics

* `pit`
* `bias`
* `sharpness`
* `crps`
* `dss`
* `brier_score`
* `interval_score`

More information on the different metrics and examples can be found in the 
[package vignette](https://cran.rstudio.com/web/packages/scoringutils/vignettes/scoringutils.html). 

