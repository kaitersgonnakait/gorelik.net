---
layout: post
title: "In defense of three-dimensional graphs"
date: 2018-05-28
categories: 
  - "blog"
tags: 
  - "3d"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "density-plot"
  - "joyplot"
---

"There is only one thing worse than a pie chart. It's a 3-D pie chart". This is what I used to think for quite a long time. Recently, I have revised my attitude towards pie charts, mainly due to the [works of Rober Kosara](https://eagereyes.org/blog/2016/an-illustrated-tour-of-the-pie-chart-study-results) from Tableau. I am no so convinced that pie charts can be a good visualization choice, I even included a session "[Pie charts as an alternative to bar charts](https://github.com/bgbg/datascience_dataviz_workshop/blob/master/03-pie%20charts%20as%20an%20alternative%20to%20bar%20charts-inclass.ipynb)" in my recent workshop.

What about three-dimensional graphs? I'm not talking about the situations where the data is intrinsically three-dimensional. Such situations lie within the consensus. I'm talking about adding a third dimension to graphs that can work in two dimensions. Like the example below that is taken from a [2017 post by Deven Wisner](https://devenwisner.com/2017/06/27/to-3d-or-not-to-3d-that-is-the-question/).

![Screenshot: a 3D pie chart with text "The only good thing about this pie chart is that it's starting to look more like [a] real pie"](/assets/images/2018/05/screen-shot-2018-05-28-at-14-41-43.png?w=600)

Of course, this is not a hypothetical example. We all remember how the late Steve Jobs tried to create a false impression of Apple market share

![Steve Jobs during a presentation, in front of a ](/assets/images/2018/05/screen-shot-2018-05-28-at-14-56-38.png?w=2048)

Having said all that, **can you think of a legitimate case where adding the third dimension adds more value than distraction?** I worked hard, and I finally found it.

 

Take a look at the overlapping density plot (a.k.a "joy plot").

![Three joyplot examples](/assets/images/2018/05/joyplots.jpg)

If you think of this, joyplots are nothing more than 3-d line graphs done well. Most of the time, they provide information-rich data overview that also enables digging into fine details. I really like joyplots. I included one [in my recent workshop](https://github.com/bgbg/datascience_dataviz_workshop/blob/master/01-drastically-different-time-series.ipynb). Many libraries now provide ready-to-use implementations of joyplots. This is a good thing to have. The only reservation that I have about those implementations is the fact that many of them, including my [favorite seaborn](https://seaborn.pydata.org/examples/kde_joyplot.html), add meaningless colors to the curves. But this is a topic for another rant.
