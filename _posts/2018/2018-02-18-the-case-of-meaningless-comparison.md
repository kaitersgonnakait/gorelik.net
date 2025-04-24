---
layout: post
title: "The case of meaningless comparison"
date: 2018-02-18
categories: 
  - "blog"
tags: 
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "time-series"
  - "worst-practice"
coverImage: "/assets/images/2018/02/screen-shot-2018-02-18-at-15-48-14.png"
---

Exposé, an Australian-based data analytics company, published a [use case in which they analyze the benefits of a custom-made machine learning solution](https://exposedata.wordpress.com/2018/02/18/water-consumption-prediction-our-sa-water-case-study/). The only piece of data in their report \[[PDF](https://exposedata.files.wordpress.com/2018/02/exposc3a9-case-study-sawater-predictive.pdf)\] was a graph which shows the observed and the predicted

![Screenshot that shows two time series curves: one for the observed and one for the predicted values](/assets/images/2018/02/screen-shot-2018-02-18-at-14-21-24.png)

Graphs like this one provide an easy-to-digest overview of the data but are meaningless with respect to our ability to judge model accuracy. When predicting values of time series, it is customary to use all the available data to predict the next step. In cases like that, "predicting" the next value to be equal to the last available one will result in an impressive correlation. Below, for example, is my "prediction" of Apple stock price. In my model, I "predict" tomorrow's prices to be equal to today's closing price plus random noise.

![Two curves representing two time series - Apple stock price and the same data shifted by one day](/assets/images/2018/02/aapl_stock_price.png)

Look how impressive my prediction is!

I'm not saying that Exposé constructed a nonsense model. I have no idea what their model is. I do say, however, that their communication is meaningless. In many time series, such as consumption dynamics, stock price, etc, each value is a function of the previous ones. Thus, the "null hypothesis" of each modeling attempt should be that of a random walk, which means that we should not compare the **actual** values but rather the **changes**. And if we do that, we will see the real nature of the model. Below is such a graph for my pseudo-model (zoomed to the last 20 points)

![diff_series](/assets/images/2018/02/diff_series.png)

 

Suddenly, my bluff is evident.

To sum up, a direct comparison of observed and predicted time series can only be used as a starting point for a more detailed analysis. Without such an analysis, this comparison is nothing but a meaningless illustration.
