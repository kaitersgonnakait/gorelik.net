---
layout: post
title: "The fastest way to get first N items in each group of a Pandas DataFrame"
date: 2017-11-27
categories: 
  - "blog"
tags: 
  - "data-science"
  - "optimization"
  - "pandas"
  - "python"
---

In my work, the speed of code writing and reading is usually more important than the speed of its execution. Right now, I'm facing a challenge of optimizing the running time of a fairly complex data science project. After a lot of profiling, I identified the major time consumers. One of such time-consuming steps involved grouping a Pandas DataFrame by a key, sorting each group by a score column, and taking first N elements in each group. The tables in this step are pretty small not more than one hundred elements. But since I have to perform this step many times, the running time accumulates to a substantial fraction.

Let's first construct a toy example

\[code lang="python"\] N = 100 x = np.random.randint(1, 5, N).astype(int) y = np.random.rand(N) d = pd.DataFrame(dict(x=x, y=y)) \[/code\]

I'll use [%%timeit cell magic](http://ipython.readthedocs.io/en/stable/interactive/magics.html) which runs a Jupyter cell many times, and measures the time it takes to run the code.

\[code lang="python"\]

%%timeit d.groupby( 'x' ).apply( lambda t: t.head(K) ).reset\_index(drop=True)

\[/code\]

This is the output:

```
3.19 ms ± 253 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
```

 

I suspected that head() was not the most efficient way to take the first lines. I tried .iloc

\[code lang="python"\]

%%timeit d.groupby( 'x' ).apply( lambda t: t.iloc\[0:K\] ).reset\_index(drop=True)

\[/code\]

```
2.92 ms ± 86.9 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
```

A 10% improvement. Not bad but not excellent either. Then I realized that Pandas groupby object have their own head function

\[code lang="python"\]

%%timeit d.groupby( 'x' ).head( K ).reset\_index(drop=True)

\[/code\]

```
674 µs ± 23.7 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

647 microseconds instead of 3.2 milliseconds. The improvement is by almost a factor of five!

It's not enough to have the right tool, it's important to be aware of it, and to use it right. I wonder whether there is even faster way to obtain this job.
