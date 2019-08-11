---
layout: post
title:  "Quest for the Bar Chart Race - Part 2"
excerpt: "In this part - we make a bar chart race on matplotlib - quickly"
date:   2019-08-11 18:29:00 +0530
categories: blog
comments: true
tag: data science, bar chart race
---

Ok, so we use the same car manufacturing countries per year example - and try making a bar chart race on matplotlib.
This attempt is a primitive approach and will not be as beautiful as Flourish, but we will have something.

Here is the jupyter lab of this attempt.

Cell by cell description of the jupyter lab:

1.	Import pandas, matplotlib and numpy library. (keep it simple)
2.	read the csv where the wikipedia table is stored.
3.	remove the unwanted columns.
4.	display the dataframe
5.	make the country the row index.
6.  to 9.
7.  to 9.
8.  to 9.
9.	 Change the datatype in the table from object to float64
11.	Fill all NaN values with zero.
12.	Make the countrys columns from row index to a column again.
13. to 18.
12. 
13. 
14. 
15. 
16. 
17. 
18.	take each year, sort the countries by car production and plot them on a horizontal barchart.

Once we have all the images, they can be assembled into a gif using Python again. Not doing that for this attempt because I know the results are not going to be very impressive. Let us give it a more detailed look in the next post.

Note: The notebook got really dirty at some point of time with trying all the different things. The one uploaded is a cleaned up version.
