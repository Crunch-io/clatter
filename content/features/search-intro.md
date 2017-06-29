+++
title = "Searching on Crunch (just got better)"
description = "A brief overview of our search capability, some of the tech behind it, and what's new."
date = "2017-06-30T12:59:58-04:00"
weight = 20
draft = false
tags = []
categories = ["general", "search"]
+++

If you've been using Crunch's web application for a while, you probably noticed a large white box in the corner with a magnifying glass.
As unassuming as this little entry box is, there's a lot going on behind the scenes to make this possible.  Our goal
is to make an interface that is both natural and effective at helping you find the data you are looking for in your
collection of datasets.

Search has become an expected feature for anyone doing anything web-based.  At Crunch we understand this process
should be simple, integrated, and seamless within your workflows.

Everything starts when you import your data into Crunch.  Whether through our API, rcrunch, pycrunch, directly through
the web app or working with our team for your large-scale custom implementation, your dataset's metadata is cataloged
in a central repository so that you can access all of your data at once.  Don't worry, we make special efforts to
ensure that your data is only accessed by those who are allowed to see it.  This process of catalogging is called
"indexing".  What indexing does is to allow us to enable rapid searching, since the algorithms that would be required
to match your search query with a result is precomputed.  Without this capability we would be limited to very simple
searching methods based on the sheer horsepower searching requires.
 
{{< figure src="../images/SearchFilter.png" class="floating-right">}}

With the help of Elasticsearch, we are able to have a broad range of search capabilities, as well as have a good scaling story.
Elasticsearch enables us to utilize complex search algorithms, and implement different ones in the future as our customer's
needs grow.  It also enables us to manage new search features while offering zero-downtime to our users, but that is a story
for another post.  One of the main reasons we chose Elasticsearch to serve you is that the scaling methodology is built-in.
This means that as our customer demand increases, we can increase the resources on our end to meet that demand without
having to come up with new architecture and change thousands of lines of code.


This week we are rolling out search filtering, which allows you to filter your results by type and when the survey
ended.  We found that our users sometimes were looking for a particular category name, or wanted to find just a 
particular dataset they used in the past few months, and this is a lot easier to do if you are able to refine your
results a bit.  In fact, we are making quite a few changes to search in the coming months to enable all sorts
of new workflows, so keep checking back for more info about that!