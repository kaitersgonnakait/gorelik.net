---
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
layout: "post"
---

<!-- wp:paragraph -->
I recently rediscovered a **volcano plot** -- a scatter plot that aims to visualize changes in large populations.


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Volcano plots are very technical and specialized and, most probably, are not a good fit for explanatory data visualization. However, they can be useful during the exploration phase, and they come with a set of well-established metrics. 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Moreover, if you are lucky enough to have well-behaved data, the plots look very cool


<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://galaxyproject.github.io/training-material/topics/transcriptomics/images/rna-seq-viz-with-volcanoplot/volcanoplot.png" alt="Visualization of RNA-Seq results with Volcano Plot"><figcaption>From <a href="https://training.galaxyproject.org/training-material/topics/transcriptomics/tutorials/rna-seq-viz-with-volcanoplot/tutorial.html">here</a></figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
Of course, in real life, the data is messy. Add bad visualization practices to the mess and you get a marvel like this one


<!-- /wp:paragraph -->

<!-- wp:image {"id":3770,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="/assets/img/2020/12/image-8.png" alt="" class="wp-image-3770"><figcaption>From <a href="https://science.sciencemag.org/content/early/2020/12/09/science.abb5920">here</a></figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
The bottom line: if you have two populations to compare, consider volcano plots. But do remember dataviz good practices.


<!-- /wp:paragraph -->
