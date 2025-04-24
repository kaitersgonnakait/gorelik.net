---
layout: post
title: "Before and after: Alternatives to a radar chart (spider chart)"
date: 2020-11-10
categories: 
  - "blog"
tags: 
  - "bar-plot"
  - "before-after"
  - "data-visualisation"
  - "data-visualization"
  - "radar-chart"
  - "spider-chart"
---

A radar chart (sometimes called "spider charts") look cool but are, in fact,  
pretty lame. So much so that when the data visualization author Stephen Few mentioned them in his book [Show me the numbers](https://www.amazon.com/Show-Me-Numbers-Designing-Enlighten/), he did so in a chapter called "Silly graphs that are best forsaken."

Here, I will demonstrate some of its problems, and will suggest an alternative

## Before: The problems of a radar (spyder) plot

![](/assets/images/2020/11/image-1.png?w=578)

Above is my reconstruction of the original plot that I saw in a Facebook discussion. The graph looks pretty cool, I have to admit, but it is full of problems.  
What are the problems of a spyder plot or a radar plot?  
Let's start with readability. Can you quickly tell the value of "Substance abuse" for the red series? Not that easy.

But a more significant problem emerges when one realizes that in most cases, the order of the categories is arbitrary and that different sorting options may result in entirely different visual pictures.  

![](/assets/images/2020/11/image-2.png?w=1024)

## After: conclusion-based graph design

I have been continually preaching to add meaningful titles to all the graphs you are creating. (See [How to suck less in data visualization and professional communication](https://gorelik.net/2020/07/28/how-to-suck-less-in-data-visualization-and-professional-communication/)).

One of the byproducts of adding a title is the fact that when you write down your main takeaway of a graph, you force yourself to think, "does this graph show what it says it shows?" Thus, you guide yourself to better graph choices.

Let's say that we conclude that there is no correlation between the two series of data. Is this conclusion evident from the graphs? I would say, not so much.

Instead of a radar chart, I suggest creating two aligned, horizontal graph plots. This way, we may sort one subplot according to the values, and then, correlation (or lack of thereof) will be evident.

![](/assets/images/2020/11/image-3.png?w=712)

But what if we noticed something interesting about the differences between A and B groups? If this is true, let's show precisely this: the differences.

![](/assets/images/2020/11/image-5.png?w=870)

Notice how the bars in this version are sorted according to the difference. Sorting a bar chart is the easiest way to make it readable.

Python code that I used to create these graphs is available here https://gist.github.com/bgbg/db833db723998cd244b5049bfe01f5ac
