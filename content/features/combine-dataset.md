+++
date = "2017-05-01T23:20:47-04:00"
draft = false
title = "Combine Datasets"
description = "Users can now combine datasets in order to create Trending"
weight = 20
tags = ["combine"]
categories = ["feature"]
+++

One of the frequently asked-for feature is to allow crunchers to visualize how a particular variable changes over time.
For instance, you might want to look at how the perceived sincerity of a candidate changes over time.  Your
data might already be saved in "waves".  The combine datasets feature will allow you to bring all of that data
into one place.


## Select a variable to trend on
Click the "+" at the bottom left of the screen.  Select "combine datasets".  This will prompt the search panel
to pop open.  Search for a variable you would like to create a trend with, and matching variables will appear with
the datasets that contain them below.  If more than one dataset matches, when you hover over the search entry 
the "combine datasets" link will appear, this is your entry point for creating a combined dataset.

## Choose which datasets you'd like to see in the trend
After selecting your trending variable, a screen will appear.  All of the datasets that match the variable you
selected will appear.  At this point you can select or deselect the given datasets. If you want to include
datasets that don't have a matching variable (but may match ther variables you want to trend) you can click the
link on the right to show other datasets.  If you had a project  selected when you started combining, all of 
the datasets in your projects will appear.  If you were in your personal project, personal project datasets will appear.

## Maybe there are other variables you would like to trend?
Once you've selected the datasets you want to trend, you will be able to select which variables you want to
include in your combined dataset.  Use the filter to find the variables you would like to include.  The interface
remembers which variables you have clicked even if they aren't displayed.

## Click Combine!
When you are done selecting your variables, there's a few options that you can pick before clicking combine.
It may take some time to combine your datasets, but when you are finished you should be able to go directly
to your new dataset complete with a time trend of the variable you chose at the beginning.


## A few caveats

1) Datasets need an end date or start date defined to automatically create the dashboard with the trending variable.
   You may define the end date and start date for your datasets under properties.
2) Variables that you would like combined need to have the same alias, as this is what the system currently keys on
   for correlation.
3) Right now your datasets must have a combined row count of 500,000.

## Future Improvements

On the roadmap for crunch is a better way of tracking variables across datasets, using tools like machine learning and
fuzzy matching in order to match datasets.  We are planning on keeping track of what matched after combining to make
combining easier and more accurate in the future!  We'd also like to eliminate the limitation on number of rows that
the target dataset can contain.