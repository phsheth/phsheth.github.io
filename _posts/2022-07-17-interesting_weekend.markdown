---
layout: post
title:  "Interesting Weekend"
excerpt: "A look at machine learning for mechanical properties from checmical composition of metals."
date:   2022-07-17 22:40:00 +0530
categories: blog
comments: true
tag: machine learning, mechanical engineering
---

Ever since I started learning machine learning, I have been looking for applications within mechanical engineering.

Recently I came across a post on LinkedIn by a mechanical engineer who made a machine learning model for a 'low alloy steel' material data set.

The data set had chemical composition, tensile strength and elongation at increasing temperatures. I tried to find the source of the data and realised that it did not have a citable source.

So I started looking for another legitimate data source and stumbled upon an open source material data mining library called "MatMiner" by the Lawrence Berkeley National Laboratory [lbl.gov].

Within MatMiner are included some datasets that can be used for the library, one of the datasets is called "steel_strength" which contains the chemical composition, yield strength [MPa], tensile strength [MPa] and elongation [%].

Now that we have a "Citable" and "credible" data source (which has already been cleaned) - we can perform some exploratory data analysis on it.

What further comes in mind is - what can we do with this data - apart from building a chemical composition to strength "predictor" model:
1. We can build a learning tool which can help us visualise - adding which material to the steel increases its strength.
2. Further visualise the stress-life and strain-life effect from chemical composition perspecitve.
3. many other applications!

More updates in coming days!
