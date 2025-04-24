---
layout: post
title: "Bootstrapping the right way?"
date: 2019-10-06
categories: 
  - "blog"
tags: 
  - "bootstrapping"
  - "data-science"
  - "overfitting"
  - "reblog"
coverImage: "/assets/images/2019/10/revenue-confidence-intervals-2.png"
---

Many years ago, I terribly overfit a model which caused losses of a lot of shekels (a LOT). It's not that I wasn't aware of the potential overfitting. I was. Among other things, I used several bootstrapping simulations. It turns out that I applied the bootstrapping in a wrong way. My particular problem was that I "forgot" about confounding parameters and that I "forgot" that peeping into the future is a bad thing.

Anyhow, Yanir Seroussi, my coworker data scientist, gave a very good talk on bootstrapping.
