---
layout: post
title: "An example of a very bad graph"
date: 2022-03-08
categories: 
  - "blog"
tags: 
  - "bad-practice"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "rant"
---

# An example of a very bad graph

Nature Medicine is a peer-reviewed journal that belongs to the very prestigious Nature group. Today, I was reading a paper that included THIS GEM.

These two graphs are so bad. It looks as if the authors had a target to squeeze as many data visualization mistakes as possible in a single piece of graphics.

Let's take a look at the problems.

![](/assets/images/2022/03/null.png)

- Double Y axes. Don't! Double axes are bad in 99% of cases ([exceptions do exist](https://gorelik.net/2018/02/05/in-defense-of-double-scale-and-double-y-axes/), but they are rare).
- Two subgraphs that are meant to work together have different category orders and different Y-axis scales. These differences make the comparison much harder.
- Inverted Y scale in a bar chart. Wow! This is very strange. Bizarre! It took me a while to spot this. First, I tried to understand why the line of P<0.05 (the magic value of statistics) is **above** 0.1. Then, I realized that the right Y-axis is reversed. At first, I thought, "WTF?!" but then I understood why the authors made this decision. You see, according to the [widespread statistical ritual](https://journals.sagepub.com/doi/full/10.1177/2515245918771329), the lower the "P-value" is, the more significant it is considered. The value of 1 is deemed to be non-significant at all, and the value of 0 is considered "as significant as one can have." So, in theory, the authors could have renamed the axis to "Significance" and reversed the numbers. Still, the result would not be a real "significance," nor would the name be intuitive to anyone familiar with statistical analysis. On the other hand, they **really** wanted more "significant" values to be bigger than less significant ones. So, what the heck? Let's invert the scale! Well, no, this is not a good idea
- Slanted category labels. This might be a matter of taste, but I dislike rotated and slanted labels. Turning the graph solves the need for label rotation, thus making it more readable and having zero drawbacks.

## What can be done?

I don't like criticism without improvement suggestions. Let's see what I would have done with this graph. To make this decision, I first need to decide what I want to show. According to my understanding of the paper, the authors wish to show that the two data sets are very different in determining a specific outcome. To show that, we don't need to depict both the P-value and variance (mainly since these two values are very much correlated). Thus, I will depict only show one metric. I will stick with the P-value.

I will keep the category order the same between the two subgraphs. Doing so will create a "[table lens](https://www.perceptualedge.com/articles/b-eye/tablelens.pdf)" effect; it will show the individual values while demonstrating the lack of correlations between the two groups. Finally, I will convert the bars into points, primarily to reduce the data-ink ratio. Two additional arguments against bar charts, in this case, are the facts that the P-values of a statistical test cannot possibly be zero and that bar charts don't allow log-scale, in case we'll want to use it.

The result should look like this sketch.

![](/assets/images/2022/03/null-1.png)
