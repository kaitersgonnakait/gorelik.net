---
layout: post
title: "ASCII histograms are quick, easy to use and implement"
date: 2018-02-25
categories: 
  - "blog"
tags: 
  - "ascii"
  - "code"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "histogram"
coverImage: "/assets/images/2018/02/screen-shot-2018-02-25-at-21-34-12.png"
---

![Screen Shot 2018-02-25 at 21.25.32](/assets/images/2018/02/screen-shot-2018-02-25-at-21-25-32.png?w=156)From time to time, we need to look at a distribution of a group of values. Histograms are, I think, the most popular way to visualize distributions. "Back in the old days," when most of my work was done in the console, and when creating a plot from Python was required too many boilerplate code lines, I found a neat function that produced histograms using ASCII characters.

Surely, today, when most of us work in a notebook environment, ASCII histograms aren't as useful as they used to be. However, they are still helpful. One scenario in which ASCII diagrams are useful is when you write a log file for an iterative process. A quick glimpse at the log file will let you know when the distribution of some scoring function reached convergence.

That is why I keep my version of `asciihist` updated since 2005. You may find it on Github [here](https://gist.github.com/bgbg/608d9ef4fd75032731651257fe67fc81).
