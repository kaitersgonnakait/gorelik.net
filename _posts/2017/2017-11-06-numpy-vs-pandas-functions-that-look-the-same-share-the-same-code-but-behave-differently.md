---
layout: post
title: "Numpy vs. Pandas: functions that look the same, share the same code but behave differently"
date: 2017-11-06
categories: 
  - "blog"
tags: 
  - "bug"
  - "coding"
  - "numpy"
  - "pandas"
  - "programming"
coverImage: "/assets/images/2017/11/screen-shot-2017-11-06-at-15-14-42.png"
---

I can't imagine how my professional life would have looked like without [pandas](https://pandas.pydata.org/), THE data analysis library for Python. Pandas shares much of its functionality and syntax with [numpy](http://www.numpy.org/), a fundamental package for scientific computing with Python. The reason for that is that, under the hood, pandas uses numpy. This similarity is very convenient as it allows passing numpy arrays to many pandas functions and vice versa. However, sometimes it sabs you in the back. Here is a nice example that I discovered after hours (OK, minutes) of debugging.

Let's create a numpy vector with a single element in it:

```
>>> import numpy as np

>>> v = np.array([3.14]) 

Now, let's compute the standard deviaiton of this vector. According to the definition, we expect it to be equal zero.
```

```
>>> np.std(v)
0.0
```

So far so good. No surprises.

Now, let's make a pandas Series out of our vector. A Series is basically a vector in which the elements can be indexed by arbitrary labels. What do you expect the standard deviation should be now?

```
>>> import pandas as pd
>>> s = pd.Series(v)
>>> s.std()
nan

```

What? Not a number? What the hell? It's not an empty vector! I didn't ask to perform the [corrected sample](https://en.wikipedia.org/wiki/Standard_deviation#Corrected_sample_standard_deviation) standard deviation. Wait a second...

```
>> s.std(ddof=0)
 0.0
```

Now I start getting it. Compare this

```
>>> print(np.std.__doc__)
Compute the standard deviation along the specified axis.
....
ddof : int, optional
Means Delta Degrees of Freedom. The divisor used in calculations
is ``N - ddof``, where ``N`` represents the number of elements.
By default `ddof` is zero.
```

... to this

```
>>> print(pd.Series.std.__doc__)

Return sample standard deviation over requested axis.

Normalized by N-1 by default. This can be changed using the ddof argument
....
ddof : int, default 1
degrees of freedom
```

Formally, the pandas developers did nothing wrong. They decided that it makes sense to default for normalized standard deviation when working with data tables, unlike numpy that is supposedly meant to deal with arbitrary matrices of numbers. They made a decision, they wrote it at least three times in the documentation, and yet... I didn't know that even after working with both the libraries for so long.

To sum up:

> \> s.std() nan >> v.std() 0.0 >> s == v 0 True dtype: bool

 

Beware.
