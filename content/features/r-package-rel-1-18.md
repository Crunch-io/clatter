+++
date = "2017-08-22T23:20:47-04:00"
draft = false
title = "Crunch R Package 1.18.0 Released"
description = ""
weight = 20
tags = ["R", "release", "geo"]
categories = ["feature"]
+++

We've just released version 1.18.0 of the Crunch R package. Current package users should see a message when they load the package instructing you how to update to the latest version. New users (or anyone) can install this latest release from CRAN with

    install.packages("crunch")

See README.md for further instructions.

Since the last CRAN release in June (1.17.0), some significant features have been added. A full list of changes can be found in (link), but here is an overview of the main additions.

## Mapping

* Crunch-hosted geographic data can now be set and updated. Use `geo()` on a variable to see if there is already associated geographic data.
* `addGeoMetadata()` function to match a text or categorical variable with available geodata based on the contents of the variable and metadata associated with Crunch-hosted geographic data.

## New variable builders

* Added support for case variables (#36): `makeCaseVariable()` takes a sequence of case statements to derive a new variable based on the values from other variables.
* Added a function to create interactions of variables (#42): `interactVariables()` takes two or more categorical variables and derives a new variable with the combination of each.

## Derived variable tools

* derivation, is.derived

## Multitables

Similar to the new tools for working with derived variables, there are also new methods for working with "multitables", the table header definitions composed of multiple variables that can be used interactively in the web app and to generate tab books of the dataset.

* Multitables can now be updated with `multitables(ds)[["Multitable name"]] <- ~ var1 + var2` syntax. Similarly, multitables can be deleted with `multitables(ds)[["Multitable name"]] <- NULL`. Multitables also have new `name()` and `delete()` methods.


## Assorted enhancements and fixes

There are many more changes in the release; see the full release notes for more details. A few other new functions are worth mentioning.

* Better integration with the web application. You can copy the URL from the browser in the web app and pass it to `loadDataset()` to load the same dataset in your R session. To go the other way, call `webApp()` on your R dataset object and it will open it in your web browser.
* `resetPassword()` allows you to trigger a password reset from R.
* `copyOrder()` to copy the ordering of variables from one dataset to another.
* `searchDatasets()` provides a basic interface to the Crunch search API for finding variables and datasets.
* Support for streaming data: check for received data with `pendingStream()`; append that pending stream data to the dataset with `appendStream()`.

More exciting changes are coming!
