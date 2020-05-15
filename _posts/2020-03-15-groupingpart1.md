---
layout: post
title: "Classifying Projects Part I"
date: 2020-05-15
published: True
---

# Introduction

This is the first post of what I think will be a three part series on a project I worked on a couple of years ago. I am proud of this work for being a pretty original application (I have yet to see anything similar to it) even if is not the most advanced machine learning application you'll see out there.

This post will give an overview of the work - what problem am I trying to solve and how did I attack it. The second post will go into the details of the feature engineering that I applied to the data.  The last post will then show how I used the features created described in the second post to feed into a dimensional reduction exercise (PCA) followed by clustering.

# The Problem

People and organization's poor record in estimating project costs is well documented. Projects of all sizes and types take more time, and cost more than their original estimates.  Many project estimates are made "bottoms-up".Small estimates are made of a larger projects constituent elements.  All of the small estimates are summed to give the estimate of the total project. An alternate approach to estimating is to identify similar projects that have been completed in the past and use their historical data as a basis-of-estimate for the project at hand.

As an example, take an estimate for a new home. The bottoms up approach would be to individually estimate the cost of the tasks of building the home: foundation pour, framing, wiring, dry walling, etc. Adding these tasks together gives the total cost of the home.  A top-down estimate would instead estimate the cost of the house by finding a sample of comparable homes already built, and taking the mean of the sample as the estimate for the new home. Many people are made to feel confident in the bottoms-up estimate given all of the detailed data that they entail. The top-down estimate is believed to be less accurate because of it's simplicity.

My preference is to use both approaches when making important estimates and to continue to refine the two estimates until they align. Calculating the top-down estimate is an easy matter but for one major catch - finding a sample of similar projects. This is the problem I am trying to address - how to methodically identify a sufficient sample of similar-too projects so that an estimate of a new project can be made from the distribution of historical projects. 

# The Approach

Companies that do business with the US government are required to keep detailed records of the labor and material that they expend on all projects. These records are typically kept in databases like SAP or Oracle. It is my experience that the large amount of data in these databases has not been put to good use. The methods described in this and subsequent posts show how I use the data in an SAP database to create [features](https://en.wikipedia.org/wiki/Feature_(machine_learning)) from which I perform a K-means clustering calculation to identify groupings of projects that can they be selected from to make future estimates. 
