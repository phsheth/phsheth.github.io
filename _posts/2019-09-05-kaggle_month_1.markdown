---
layout: post
title:  "First Month at Kaggle"
excerpt: "I took part in my first Kaggle competition. Probably a start of my competitive machine learning journey."
date:   2019-09-05 20:30:00 +0530
categories: blog
comments: true
tag: machine learning, competitive, data science
---

I received a (mass) email from [Dan Becker](https://www.kaggle.com/dansbecker) at [Kaggle](https://www.kaggle.com) regarding joining a learners course for competing at Kaggle. I remember Dan from his keras course at DataCamp. The course was good and showed how to take part in a Kaggle competition. After the learner's course - a learner's only competition was organised for everyone to take part.

I had considered working on Kaggle about two years back - but never got around to doing it. This push from Dan made it sort of easy for me to re-hone my machine learning implementation skills. The last ML project I had worked on was the [GE Analytics Certification](https://ph.sheth.cc/blog/2018/12/17/2018_review/) in November last year. Machine Learning as a skill is like a muscle - you don't work on it regularly - it doesn't build.

So, the learner's competition that Kaggle is hosting is [Classify forest types based on information about the area](https://ph.sheth.cc/blog/2018/12/17/2018_review/). The training data they have given is from a dataset provided by Jock A. Blackard and Colorado State University. It is a set of observations taken on 30m x 30m patch of land, which finally points to the type of tree which is the label. Our job is to come up with an accurate machine learning model that will predict the type of tree from the given data.

I started by applying the same strategy I had used for the [GE Analytics Certification](https://ph.sheth.cc/blog/2018/12/17/2018_review/) case study. But I soon found out that a single template approach may not work for all data - and the template needs modifications.

1. RobustScaler, when used for training and validation set - gave a good score, but when used on the test set, gave a very low score. Removing RobustScaler 
2. I discovered that stacking 2 or 3 classifiers works wonders. I stacked Random Forest, XGBoost, and ExtraTrees classifiers and this got me [somewhere on top of the leaderboard](https://twitter.com/_phsheth/status/1168844518143082498).
3. Next, it was a choice between hyperparameter tuning and feature selection. Since my home computer is a small Core i3, 4 GB RAM machine, it was slower than the kaggle kernel, and the Kaggle kernel itself has a nine hour limitation, after which your notebook fails. So I had to break the task into two, I selected going for feature selection first, and that too - individually for each classifier.
4. The mlxtend library [StackingCVClassifier] (http://rasbt.github.io/mlxtend/user_guide/classifier/StackingCVClassifier/#example-3-stacked-cv-classification-and-gridsearch) allows different feature sets for each classifier, so, as stated in step 3., I found optimum feature sets for each classifier and then used them for stacking, which got me an accuracy of slightly above 0.8, and [still higher on the leaderboard](https://twitter.com/_phsheth/status/1169215304053874689)! This rush of motivation has kept me going.
5. Apart from machine learning skill, you learn a lot here - You learn that when resources are scarce - you succeed by doing one thing at a time, and the temptation of doing multiple things simply doesn't bear fruit. So with only the Kaggle kernel at my disposal, this seems the best strategy.
6. Further, I tried AdaBoost and Bagging classifier, but one of them is bringing the test accuracy down, so have to avoid using them.
7. I am trying one last classifier (secret sauce) before I go ahead with the hyperparameter tuning of all the stacked classifier (one by one).

Hope this goes well, and hope I land up in the private leader board as well, also, hope to take part in more competitions as well! You can access my [Kaggle Profile here](https://www.kaggle.com/phsheth/) and [Kernels here](https://www.kaggle.com/phsheth/kernels).