+++
date = "2017-04-20T23:20:47-04:00"
draft = false
title = "Tab Book Improvements"
description = "By popular demand, Excel tab books just gained a bunch of new capabilities."
weight = 20
tags = ["tabbook", "export"]
categories = ["feature"]
+++

We first released the [tab book feature](http://support.crunch.io/crunch/crunch_tabbooks.html) a while back, and since then, we've collected a number of great suggestions for how to enrich the feature. Our recent release includes several of those enhancements, most of which are new options available to you in the "export tab book" panel.

## Export all on a single page

{{< figure src="../images/TabBookLayout.png" title="Layout options" class="floating-right">}}

The first new option is page layout. A common request we received was to be able to export all tables in a tab book to a single sheet in the Excel workbook, rather than exporting each table to its own worksheet. While having each table in its own sheet might be more readable when you're looking at just one, it is difficult in Excel to click through the tabs in a workbook to scan through the whole tab book. For browsing lots of results in Excel, scrolling down a single worksheet is often less tedious.

The default of one-table-per-sheet is unchanged, but to export a tab book with all tables stacked on a single Excel worksheet, toggle the "layout" setting in the export panel.

## Include a table of contents

Use this option to add a Table of Contents to the exported tab book. The table of contents contains links to each row variable in the tab book.

{{< figure src="../images/TabBookToC.png" class="centered-image">}}

## Enable hypothesis testing

Hypothesis testing has been enabled in multitables for some time. Now, if you have hypothesis testing enabled, when you export tab book to Excel the cell shading and p-value key will appear in the Excel spreadsheet.
![](../images/ExcelSigTest.png)

## Unweighted counts

Previously, if you requested a tab book with a weight applied to the dataset, the "N" or "base" row of counts beneath the tables were also weighted. These are now unweighted, as they are throughout the web app. This change allows you to see how many rows or observations in the dataset are used to compute each cell in the tables.  

## Let us know what you think

If you haven't downloaded a tab book recently, check them out. If you have suggestions for how we can improve them further, let us know!
