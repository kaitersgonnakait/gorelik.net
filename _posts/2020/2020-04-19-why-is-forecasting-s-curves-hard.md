---
title: "Why is forecasting s-curves hard?"
date: 2020-04-19
categories: 
 - "blog"
tags: 
 - "curve-fitting"
 - "data-science"
 - "forecast"
 - "forecasting"
 - "modelling"
 - "pk-pd"
 - "repost"
cover_image: "/assets/img/2020/04/wim-van-t-einde-e6ppicj05jg-unsplash.jpg"
layout: "post"
---

Constance Crozier ([@clcrozier](https://twitter.com/clcrozier/status/1251148890595708938) on Twitter) shared an interesting simulation in which she tried to fit a sigmoid curve (s-curve) to predict a plateau in a time-series. The result was a very intuitive and convincing animation that shows how wrong her initial forecasts were.

The matter of fact is that this phenomenon is not new at all. My first post-University job involved fitting numerous pharmacodynamics models. We always had to keep in mind that if the available data does not account for at least 95% of the maximum effect, the model will be very much suboptimal. It took me a while, but I managed to find the reference for this phenomenon [[here](https://www.sciencedirect.com/science/article/abs/pii/S0022354915499873)]. Maybe, when I have some time, I will repeat Constance Crozier's analysis, and add confidence intervals to emphasize the point.<br><br>**EDIT:** I came the conclusion that the most important takaway message of this demonstration is the necessity of reporting uncertainty with any forecast, and how small the value of a forecast is without uncertainty estimations. 

<div class=" wp-block-embed is-type-rich">
https://player.vimeo.com/video/408599958?dnt=1&amp;app_id=122963
</div>

![](https://constancecrozier.files.wordpress.com/2020/04/smart_phones.png?quality=80&strip=info&w=1600)

> S-curves (or sigmoid functions) are commonly used to model the evolution of social or biological systems over time [1]. These functions start with exponential growth, then increase linearly, and finally level off (therefore end up looking like a wonky s). Many things that we think of as exponential functions will actually follow an s-curve (otherwise […]
> 
> <cite><a href="http://constancecrozier.com/2020/04/16/forecasting-s-curves-is-hard/">Forecasting s-curves is hard — Constance Crozier</a></cite>
