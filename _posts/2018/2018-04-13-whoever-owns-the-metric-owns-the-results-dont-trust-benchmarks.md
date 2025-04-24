---
layout: post
title: "Whoever owns the metric owns the results -- don't trust benchmarks"
date: 2018-04-13
categories: 
  - "blog"
tags: 
  - "data-science"
  - "number-crunching"
  - "performance"
coverImage: "/assets/images/2018/04/stopwatch.jpeg"
---

Other factors being equal, what language would you choose for heavy numeric computations: Python or PHP? This is not a language war but a serious question. For me, the choice seems to be obvious: I would choose Python, and I'm not the only one. In [this survey](https://insights.stackoverflow.com/survey/2017#technologies-and-occupations), for example, 45% of data scientist use Python, compared to 24% who use PHP. The two sets of data scientists aren't mutually exclusive, but we do see the picture.

This is why I was very surprised when a colleague of mine suggested switching to PHP due to a [three times faster performance in a benchmark](https://blog.famzah.net/2016/02/09/cpp-vs-python-vs-perl-vs-php-performance-benchmark-2016/). I was very surprised and intrigued. Especially, when I noticed that they used a heavy number crunching for the benchmark.

In that benchmark, the authors compute prime numbers using the following Python code

\[code lang="python"\] def get\_primes7(n): """ standard optimized sieve algorithm to get a list of prime numbers --- this is the function to compare your functions against! --- """ if n < 2: return \[\] if n == 2: return \[2\] # do only odd numbers starting at 3 if sys.version\_info.major <= 2: s = range(3, n + 1, 2) else: # Python 3 s = list(range(3, n + 1, 2)) # n\*\*0.5 simpler than math.sqr(n) mroot = n \*\* 0.5 half = len(s) i = 0 m = 3 while m <= mroot: if s\[i\]: j = (m \* m - 3) // 2 # int div s\[j\] = 0 while j =6, Returns a array of primes, 2 <= p < n """ sieve = np.ones(n//3 + (n%6==2), dtype=np.bool) sieve\[0\] = False for i in range(int(n\*\*0.5)//3+1): if sieve\[i\]: k=3\*i+1|1 sieve\[ ((k\*k)//3) ::2\*k\] = False sieve\[(k\*k+4\*k-2\*k\*(i&1))//3::2\*k\] = False return np.r\_\[2,3,((3\*np.nonzero(sieve)\[0\]+1)|1)\] \[/code\]

Did you notice the problem? The code above is a pure Python code. I can't think of a good reason to use pure python code for computationally-intensive, time-sensitive tasks. When you need to crunch numbers with Python, and when the computational time is even remotely important, you will most certainly use tools that were specifically optimized for such tasks. One of the most important such tools is [numpy](http://www.numpy.org/), in which the most important loops are implemented in C++ or in Fortran. Many other packages, such as Pandas, scipy, sklearn, and others rely on numpy or other form of speed optimization.

The following snippet uses numpy to perform the same computation as the first one.

\[code lang="python"\] def numpy\_primes(n): # http://stackoverflow.com/questions/2068372/fastest-way-to-list-all-primes-below-n-in-python/3035188#3035188 """ Input n>=6, Returns a array of primes, 2 <= p < n """ sieve = np.ones(n//3 + (n%6==2), dtype=np.bool) sieve\[0\] = False for i in range(int(n\*\*0.5)//3+1): if sieve\[i\]: k=3\*i+1|1 sieve\[ ((k\*k)//3) ::2\*k\] = False sieve\[(k\*k+4\*k-2\*k\*(i&1))//3::2\*k\] = False return np.r\_\[2,3,((3\*np.nonzero(sieve)\[0\]+1)|1)\] \[/code\]

On my computer, the timings to generate primes smaller than 10,000,000 is 1.97 seconds for the pure Python implementation, and 21.4 milliseconds for the Numpy version. The numpy version is 92 times faster!

**What does that mean?**  Whoever owns the metric owns the results. Never trust a benchmark result before you understand how the benchmark was performed, and before making sure the benchmark was performed under the conditions that are relevant to you and your problem.
