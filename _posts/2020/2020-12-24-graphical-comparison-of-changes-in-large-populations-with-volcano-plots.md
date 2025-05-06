---
layout: post
title: "Graphical comparison of changes in large populations with \"volcano plots\""
date: 2020-12-24
categories: 
  - "blog"
tags: 
  - "data-visualisation"
  - "data-visualization"
  - "datavis"
  - "volcano-plot"
  - "worst-practice"
---

I recently rediscovered a **volcano plot** &mdash; a scatter plot that aims to visualize changes in large populations.

Volcano plots are very technical and specialized and, most probably, are not a good fit for explanatory data visualization. However, they can be useful during the exploration phase, and they come with a set of well-established metrics.

Moreover, if you are lucky enough to have well-behaved data, the plots look very cool

<figure>

![Visualization of RNA-Seq results with Volcano Plot](/assets/images/2020/12/volcanoplot.png)

<figcaption>

From [here](https://training.galaxyproject.org/training-material/topics/transcriptomics/tutorials/rna-seq-viz-with-volcanoplot/tutorial.html)

</figcaption>

</figure>

Of course, in real life, the data is messy. Add bad visualization practices to the mess and you get a marvel like this one

<figure>

![](/assets/images/2020/12/image-8.png?w=1024)

<figcaption>

From [here](https://science.sciencemag.org/content/early/2020/12/09/science.abb5920)

</figcaption>

</figure>

The bottom line: if you have two populations to compare, consider volcano plots. But do remember dataviz good practices.
