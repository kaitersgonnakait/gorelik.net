---
layout: post
title: "Data science tools with a graphical user interface"
date: 2019-11-05
categories: 
  - "blog"
tags: 
  - "data-science"
  - "gui"
  - "knime"
  - "orange"
  - "tools"
  - "weka"
coverImage: "/assets/images/2019/11/featured_guis.png"
---

A Quora user asked about data science tools with a graphical user interface. Here's [my answer](https://qr.ae/TWP0wY). I should mention though that I don't usually use GUI for data science. Not that I think GUIs are bad, I simply couldn't find a tool that works well for me.

Of the many tools that exist, I like the most [Orange](https://orange.biolab.si/) ([https://orange.biolab.si/](https://orange.biolab.si/)). Orange allows the user creating data pipelines for exploration, visualization, and production but also allows editing the “raw” python code. The combination of these features makes is a powerful and flexible tool.

![](/assets/images/2019/11/main-qimg-8c479b6cf90427f6da5dbbad84390960)

The major drawback of Orange (in my opinion) is that is uses its own data format and its own set of models that are not 100% compatible with the Numpy/Pandas/Sklearn ecosystem.

I have made a modest contribution to Orange by adding a six-lines function that computes [Matthews correlation coefficient](https://en.wikipedia.org/wiki/Matthews_correlation_coefficient).

Other tools are [KNIME](https://www.knime.com/) and [Weka](https://www.cs.waikato.ac.nz/ml/weka/) (none of them is natively Python).

There is also [RapidMinder](https://rapidminer.com/) but I never used it.
