---
layout: post
title: "Measuring the wall time in python programs"
date: 2018-02-09
categories: 
  - "blog"
tags: 
  - "gist"
  - "python"
  - "stopwatch"
  - "timing"
---

\[UPDATE Feb 2020\]: TicToc is now a package. See [this post](https://gorelik.net/2020/02/10/tictoc-a-flexible-and-straightforward-stopwatch-library-for-python/).

Measuring the wall time of various pieces of code is a very useful technique for debugging, profiling, and computation babysitting.  The first time I saw a code that performs time measurement was many years ago when a university professor used Matlab's [tic-toc](https://www.mathworks.com/help/matlab/ref/tic.html?requestedDomain=true) pair. Since then, whenever I learn a new language, the first "serious" code that I write is a tic-toc mechanism. This is my Python Tictoc class: \[[Github gist](https://gist.github.com/bgbg/61451bc9332659be32ca)\].
