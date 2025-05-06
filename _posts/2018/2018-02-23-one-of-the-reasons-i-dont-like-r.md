---
layout: post
title: "One of the reasons I don't like R"
date: 2018-02-23
categories: 
  - "blog"
tags: 
  - "python"
  - "r"
  - "r-stats"
  - "rant"
---

I never liked R. I didn't like it for the first time I tried to learn it, I didn't like it when I had to switch to R as my primary work tool at my previous job. And didn't like it one and a half year later, when I was comfortable enough to add R to my CV, right before leaving my previous job.

Today, I was reminded of one feature (out of so many) that made dislike R. It's its import (or `library`, as they call it in R) feature. In Python, you can `import a_module` and then use its components by calling `a_model.a_function`. Simple and predictable. In R, you have to read the docs in order to understand what will happen to your namespace after you have `library(a.module)` (I know, those dots grrrr) in your code. This feature is so annoying that people write modules that help them using other modules. Like in [this blog post](http://\(https://trinkerrstuff.wordpress.com/2018/02/22/minimal-explicit-python-style-package-loading-for-r/), which looks like an interesting thing to do, but ... wouldn't it be easier to use Python?
