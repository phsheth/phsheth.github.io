---
layout: post
title:  "The Python globals() Function"
excerpt: "A look into the python globals() functionality."
date:   2019-12-04 11:54:00 +0530
categories: blog
tag: python
---

I recently participated in a company organised Hackathon at work. Apart from learning how to come up with a quick machine learning model, I learnt a lot of other things as well in the process. One of them is the Python globals() function.

Now, I always wanted to create variables within a for-loop, on the go, but never got around to doing that. During this hackathon - the need arose again. So, I was looking at stackexchange for clues, and stumbled upon the globals() functionality.

To give a bit of a context to the problem, and as an example, say we are working on an engine dynamics problem, and we want to make arrays for different orders.

We make an array with the orders and a variable with a single engine speed.
Now, to plot it on a campbell diagram, and refer back to it later (for capturing the crossings with engine speeds and modes to the frequencies at various orders), we will need variables for each order.

The globals() function helps us name and refer these variables further down the line in the same code.
The unique advantage here is - variable names that are created with a for-loop with globals(), can have decimals in their names as well!

Below is a Jupyter Lab gist - which will explain what the globals() function does!
Do let me know if you have used globals() in this, or any other manner in your code!

{% gist 7b50bf89f6a426b4d27baecbe3454dd6 %}
