---
layout: post
title:  "Quest for the Bar Chart Race - Part 1"
excerpt: "There have been many bar chart races around me, this is my look at how to create a bar chart race, from easy to difficult."
date:   2019-07-30 16:30:00 +0530
categories: data science, blog, bar chart race
comments: true
tag: bar chart race
---

So, there have been many bar chart race [BCR henceforth] visualisations around on the internet. The latest one was used by Formula 1 to show driver positions and visualising the entire race on a bar chart. BCRs are pretty cool. They are animated, and show the position, and progress dynamically.

In this part - I will use the easiest method to create a bar chart race - [Flourish](https://app.flourish.studio)

Using [Flourish](https://app.flourish.studio) is pretty nifty. But, it is better to clean and prepare the data outside to be conducive to the [Flourish](https://app.flourish.studio) environment.

The data we will look to convert to a BCR is from Wikipedia: [List of countries by motor vehicle production](https://en.wikipedia.org/wiki/List_of_countries_by_motor_vehicle_production)

Now let me be honest with you - I started off with creating the BCR on matplotlib (yes, I think matplotlib can do it) - but ended up trying Flourish to see its various features.

Step 1: Download the table from [Wikipedia](https://en.wikipedia.org/wiki/List_of_countries_by_motor_vehicle_production).
Step 2: Clean the table by removing references in square brackets, save it as a csv file.
Step 3: Read the csv file in Flourish.
Step 4: Go back to pandas and sort the data because Flourish reads from left to right - if the first column is year 2018 and last is 1950 - your Flourish BCR with start from 2018 and end at 1950. Hence, sort first. Save it back as a csv.
Step 5: Explore all the options on Flourish - add the title, and footer text appropriately.
Step 6: And voila - you have a BCR ready to publish or embed:


<div class="flourish-embed" data-src="visualisation/551072"></div><script src="https://public.flourish.studio/resources/embed.js"></script>
