---
layout: post
title: "Useful redundancy -- when using colors is not completely useless"
date: 2018-11-26
categories: 
  - "blog"
tags: 
  - "because-you-can"
  - "colors"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "israel"
  - "redundancy"
coverImage: "/assets/images/2018/11/featured.png"
---

The maximum data-ink ratio principle implies that one should not use colors in their graphs if the graph is understandable without the colors. The fact that you can do something, such as adding colors, doesn't mean you should do it. I know it. [I even have a dedicated tag on this blog for that](https://gorelik.net/tag/because-you-can/). Sometimes, however, consistent use of colors serves as a useful navigation tool in a long discussion. Keep reading to learn about the justified use of colors.

Pew Research Center is a "is a nonpartisan American fact tank based in Washington, D.C. It provides information on social issues, public opinion, and demographic trends shaping the United States and the world." Recently, I read a report prepared by the Pew Center on the [religious divide in the Israeli society](http://www.pewforum.org/2016/03/08/israels-religiously-divided-society/). This is a fascinating report. I recommend reading without any connection to data visualization.

But this post does not deal with the Isreali society but with graphs and colors.

Look at the first chart in that report. You may see a tidy pie chart with several colored segments. 

![Pie chart: Religious composition of Israeli society. The chart uses several colored segments](/assets/images/2018/11/screen-shot-2018-11-26-at-10-49-51.png)

Aha! Can't they use a single color without losing the details? Of course the can! A monochrome pie chart would contain the same information:

![Pie chart: Religious composition of Israeli society. The chart uses monochrome segments](/assets/images/2018/11/screen-shot-2018-11-26-at-10-49-512.png)

In most of the cases, such a transformation would make a perfect sense. In most of the cases, but not in this report. This report is a multipage research document packed with many facts and analyses. The pie chart above is the first graph in that report that provides a broad overview of the Israeli society. The remaining of this report is dedicated to the relationships between and within the groups represented by the colorful segments in that pie chart. To help the reader navigating through this long report, its authors use a consistent color scheme that anchors every subsequent graph to the relevant sections of the original pie chart.

- ![](/assets/images/2018/11/screen-shot-2018-11-26-at-11-06-30.png?w=656)
    
- ![](/assets/images/2018/11/screen-shot-2018-11-26-at-11-07-44.png?w=656)
    
- ![](/assets/images/2018/11/screen-shot-2018-11-26-at-11-06-53.png)
    

All these graphs and tables will be readable without the use of colors. Despite the fact that the colors here are redundant, this is a **useful redundancy**. By using the colors, the authors provided additional **information layers** that make the navigation within the document easier. I learned about the concept of useful redundancy from "[Trees, Maps, and Theorems](http://www.treesmapsandtheorems.com/)" by Jean-luc Dumout. If you can only read one book about data communication, it should be this book.
