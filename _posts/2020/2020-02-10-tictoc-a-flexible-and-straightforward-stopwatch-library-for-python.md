---
title: "TicToc &mdash; a flexible and straightforward stopwatch library for Python."
date: 2020-02-10
categories: 
 - "blog"
tags: 
 - "code"
 - "open-source"
 - "python"
 - "tictoc"
layout: "post"
cover_image: /assets/img/2020/02/pexels-photo-2388570.webp
---

Many years ago, I needed a way to measure execution times. I didn't like the existing solutions so I wrote my own class. As time passed by, I added small changes and improvements, and recently, I decided to publish the code on GitHub, [first as a gist](https://gorelik.net/2018/02/09/measuring-the-wall-time-in-python-programs/), and now as a full-featured [Github repository](https://github.com/bgbg/tictoc), and a [pip package](https://pypi.org/project/tictoc-borisgorelik/).

# TicToc - a simple way to measure execution time

TicToc provides a simple mechanism to measure the wall time (a stopwatch) with reasonable accuracy.

Crete an object. Run tic() to start the timer, toc() to stop it. Repeated tic-toc's will accumulate time. The tic-toc pair is useful in interactive environments such as the shell or a notebook. Whenever toc is called, a useful message is automatically printed to stdout. For non-interactive purposes, use start and stop, as they are less verbose.

Following is an example of how to use TicToc:

## Usage examples

    def leibniz_pi(n):
        ret = 0
        for i in range(n * 1000000):
            ret += ((4.0 * (-1) ** i) / (2 * i + 1))
        return ret
    
    tt_overall = TicToc('overall')  # started  by default
    tt_cumulative = TicToc('cumulative', start=False)
    for iteration in range(1, 4):
        tt_cumulative.start()
        tt_current = TicToc('current')
        pi = leibniz_pi(iteration)
        tt_current.stop()
        tt_cumulative.stop()
        time.sleep(0.01)  # this inteval will not be accounted for by `tt_cumulative`
        print(
            f'Iteration {iteration}: pi={pi:.9}. '
            f'The computation took {tt_current.running_time():.2f} seconds. '
            f'Running time is {tt_overall.running_time():.2} seconds'
        )
    tt_overall.stop()
    print(tt_overall)
    print(tt_cumulative)


TicToc objects are created in a "running" state, i.e you don't have to start them using `tic`. To change this default behaviour, use

    tt = TicToc(start=False)
    # do some stuff
    # when ready
    tt.tic()


## Installation

Install the package using pip

`pip install tictoc-borisgorelik`
