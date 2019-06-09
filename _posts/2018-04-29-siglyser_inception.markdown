---
layout: post
title:  "SigLyser - Inception"
excerpt: "My first attempt at developing a software for people."
date:   2018-04-29 13:54:00 +0530
categories: blog
comments: true
tag: python, scipy
---
I had been tinkering around the idea of making an open source signal processing application for a long time. I started building SigLyser around Scilab in 2014. After creating a basic GUI - I found Scilab lacking to handle the data structure and also the GUI making part. After learning Python - I found it a better candidate  and decided to move SigLyser to Python.

SigLyser will be built as a web application - using Flask.

Initial data reading using Pandas. Further - converted to NumPy arrays.

The signal processing calculations will be done the the SciPy modules of fftpack and signal.

Plotting is done using the Bokeh library.

Code repository: https://github.com/siglyser/siglyser

Code Running: https://siglyser.herokuapp.com/

Project page: https://siglyser.github.io

Blog: https://siglyser.wordpress.com

The project is at a very early stage - I will start looking for contributors once the project reaches a certain stage.

Update on 09 June 2019:
Still haven't progressed much beyond the initial release. Have to pickup on all projects as time permits.
