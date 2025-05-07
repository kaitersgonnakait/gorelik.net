---
title: "In defense of double-scale and double Y axes"
date: 2018-02-05
categories: 
 - "blog"
tags: 
 - "best-practice"
 - "data-visualisation"
 - "data-visualization"
 - "dataviz"
 - "double-scale"
 - "opinion"
cover_image: "/assets/img/2018/02/screen-shot-2018-02-05-at-13-20-15.png"
layout: "post"
---

If you had a chance to talk to me about data visualization, you know that I dislike the use of double Y-axis for anything except for presenting different units of the same measurement (for example inches and meters). Of course, I'm far from being a special case.  Double axis ban is a standard stand among all the people in the field of data visualization education. Nevertheless, double-scale axes (mostly Y-axis) are commonly used both in popular and technical publications. One of my data visualization students in the Azrieli College of Engineering of Jerusalem told me that he continually uses double Y scales when he designs dashboards that are displayed on a tiny screen in a piece of sophisticated hardware. He claimed that it was impossible to split the data into separate graphs, due to space constraints, and that the engineers that consume those charts are professional enough to overcome the shortcomings of the double scales. I couldn't find any counter-argument.

When I tried to clarify my position on that student's problem, I found an interesting article by Financial Times commentator John Auther, called "Lies, Damned Lies and Statistics." In this article, John Auther reviews the many problems a double scale can create. He also shows different alternatives (such as normalization). However, at the end of that article, John Auther also provides strong and valid arguments in favor of the moderate use of double scales. John Auther notices strange dynamics of two metrics

[caption id="attachment_2022" align="alignnone" width="1466"]![A chart with two Y axes - one for EURJPY exchange rate and the other for SPX Index](/assets/img/2018/02/screen-shot-2018-02-05-at-13-13-34.png){:width="1466"} Screenshot from the article https://t.co/UYVqZpSzdS (Financial Times)[/caption]

> It is extraordinary that two measures with almost nothing in common with each other should move this closely together. In early 2007 I noticed how they were moving together, and ended up writing an entire book attempting to explain how this happened.


It is relatively easy to modify chart scales so that "two measures with almost nothing in common [...] move [...] closely together". However, it is hard to argue with the fact that it was the double scale chart that triggered that spark in the commentator's head.  He acknowledges that normalizing (or rebasing, as he puts it) would have resulted in a similar picture

[caption id="attachment_2023" align="alignnone" width="1462"]![Graph that depicts the dynamics of two metrics, brought to the same scale](/assets/img/2018/02/screen-shot-2018-02-05-at-13-13-43.png){:width="1462"} Screenshot from the article https://t.co/UYVqZpSzdS (Financial Times)[/caption]

But

> However, there is one problem with rebasing, which is that it does not take account of the fact that a stock market is naturally more variable than a foreign exchange market. Eye-balling this chart quickly, the main message might be that the S&P was falling faster than the euro against the yen. The more important point was that the two were as correlated as ever. Both stock markets and foreign exchange carry trades were suffering grievous losses, and they were moving together — even if the S&P was moving a little faster.


I am not a financial expert, so I can't find an easy alternative that will provide the insight John Auther is looking for while satisfying my purist desire to refrain from using double Y axes. The real question, however, is whether such an alternative is something one should be looking for. In many fields, double scales are the accepted language. Thanks to the standard language, many domain experts are able to exchange ideas and discover novel insights.  Reinventing the language might bring more harm than good. Thus, my current recommendations regarding double scales are:

**Avoid double scales when possible, unless its a commonly accepted practice. In which case, be persistent and don't lie.**

 
