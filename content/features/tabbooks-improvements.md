+++
date = "2017-04-20T23:20:47-04:00"
draft = false
title = "Tabbooks Improvements"
description = "We've made tab books more flexible and more closely formatted them to multitables."
weight = 20
tags = ["tabbooks"]
categories = ["feature"]
+++

# Welcome to the Dev Blog

First of all, welcome to the Crunch.io development blog. We’ll be using this space to tell you about new features and to occasionally give you some insight into how Crunch works.

Today I’m going to go over some of the recent changes to the tab books you can export through the multitable interface.

# New Export Options – Table of Contents and Single-Page Export

We’ve added a couple frequently requested options when you create a tab book. You’ll see them when you select Export tab book in the Multitable interface.

## Layout
Layout determines whether the tab book will display one row variable per Excel sheet or export the entire tab book on a single sheet.  
![](../images/TabbookLayout.png)

## Table of Contents
Use this option to add a Table of Contents to the exported tab book. The table of contents contains links to each row variable in the tab book.
![](../images/TabBookToC.png)

# Hypothesis Testing
Hypothesis testing has been enabled in multitables for some time. Now, if you have hypothesis testing enabled, when you export tab book to Excel the cell shading and p-value key will appear in the Excel spreadsheet.
![](../images/ExcelSigTest.png)

# Unweighted N Totals
A request we’ve had from several users is to include unweighted totals in tab books, so these are now included in the exported Excel files.

That’s all for now. Watch this space for more new features and other items of interest.
