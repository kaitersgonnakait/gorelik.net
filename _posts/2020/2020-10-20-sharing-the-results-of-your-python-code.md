---
title: "Sharing the results of your Python code"
date: 2020-10-20
categories: 
 - "blog"
tags: 
 - "panel"
 - "python"
 - "sharing"
 - "streamlit"
layout: "post"
---

If you work, but nobody knows about your results or cares about them, have you done any work at all?

![](/assets/img/2020/10/pexels-photo-38136.jpeg)

A proverbial tree in the proverbial forest. Photo by veeterzy on [Pexels.com](https://www.pexels.com/photo/nature-forest-trees-park-38136/)

As a data scientist, the product of my work is usually an algorithm, an analysis, or a model. What is a good way to share these results with my clients?

Since 99% of my time, I write in Python, I fell in love with a framework called Panel (http://panel.holoviz.org/). Panel allows you to create and serve basic interactive UI around data, an analysis, or a method. It plays well with API frameworks such as [FastAPI](https://fastapi.tiangolo.com/) or [Flask](https://flask.palletsprojects.com/).  The only problem is that to share this work. Sometimes, it is enough to run a local demo server, but if you want to share the work with someone who doesn't sit next to you, you have to host it somewhere and to take care of access rights. For this purpose, I have a cheap cloud server ($5/month), which is more than enough for my personal needs.

If you can share the entire work publicly, some services can pick up your Jupyter notebooks from  Github and interactively serve them. I know of [voila](http://voila.readthedocs.io/)  and [Binder](https://mybinder.org/))

Recently, S[treamlit.io](http://streamlit.io/) is entering this niche. It currently only allows sharing public repos, but promises to add a paid service for your private code. I’m eager to see that.