---
layout: post
title:  "Finding Roots of Equations using Scipy Optimize"
excerpt: "Checking excerpt capability."
date:   2019-05-20 13:12:00 +0530
categories: blog
tag: python, scipy
---

TESTING POST

I came across a requirement for finding two unknows with two equations. Whilst Excel and MathCAD would make the task easier to some extent, achieving this using Python requires a bit of time and understanding.


{% gist 7b50bf89f6a426b4d27baecbe3454dd6 %}


```python
for i in order_list:
    globals()['order_%s' % i] = np.array([i])
    print ("Engine %s" % i, "Order:", globals()['order_%s' % i])
```

<img src="https://latex.codecogs.com/png.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" />
