---
layout: post
title:  "Finding Roots of Equations using Scipy Optimize"
date:   2019-05-20 13:12:00 +0530
categories: blog
tag: python, scipy
---

I came across a requirement for finding two unknows with two equations. Whilst Excel and MathCAD would make the tatk


{% gist 7b50bf89f6a426b4d27baecbe3454dd6 %}


```python
for i in order_list:
    globals()['order_%s' % i] = np.array([i])
    print ("Engine %s" % i, "Order:", globals()['order_%s' % i])
```
