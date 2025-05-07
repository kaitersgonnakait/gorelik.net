---
title: "Error bars in bar charts. You probably shouldn't"
date: 2019-10-07
categories: 
 - "blog"
tags: 
 - "because-you-can"
 - "data-visualisation"
 - "data-visualization"
 - "dataviz"
 - "gigerenzer"
 - "uncertainty"
layout: "post"
---

<!-- wp:paragraph -->
This is another post in the series [Because You Can](https://gorelik.net/tag/because-you-can/). This time, I will claim that the fact that you can put error bars on a bar chart doesn't mean you should.


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
It started with a paper by prof. Gerd Gigerenzer whose work in promoting numeracy I adore. The paper, "[Natural frequencies improve Bayesian reasoning in simple and complex inference tasks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4604268/)" contained a simple graph that meant to convince the reader that natural frequencies lead to more accurate understanding (read the paper, it explains these terms). The error bars in the graph mean to convey uncertainty. However, the data visualization selection that Gigerenzer and his team selected is simply wrong. 


<!-- /wp:paragraph -->

<!-- wp:image {"id":2635,"sizeSlug":"large"} -->
<figure class="wp-block-image size-large"><img src="/assets/img/2019/10/image-1.png" alt="" class="wp-image-2635"></figure>
<!-- /wp:image -->

<!-- wp:image {"align":"right","id":2656,"width":122,"height":236,"sizeSlug":"large","linkDestination":"custom"} -->
<div class="wp-block-image"><figure class="alignright size-large is-resized"><a href="https://amzn.to/2MngEru"><img src="/assets/img/2019/10/image-3.png" alt="" class="wp-image-2656" width="122" height="236"></a></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
First of all, look at the leftmost bar, it demonstrates so many problems with error bars in general, and in error bars in barplots in particular. Can you see how the error bar crosses the X-axis, implying that Task 1 might have resulted in negative percentage of correct inferences?


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
The irony is that Prof. Gigerenzer is a worldwide expert in communicating uncertainty. I read his book "[Calculated risk](https://amzn.to/2MngEru)" from cover to cover. Twice. 


<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
### Why is this important? 


<!-- /wp:heading -->

<!-- wp:paragraph -->
Communicating uncertainty is super important. Take a look at this 2018 study with the self-explaining title "[Uncertainty Visualization Influences how Humans Aggregate Discrepant Information](https://www.researchgate.net/profile/Miriam_Greis/publication/324659447_Uncertainty_Visualization_Influences_how_Humans_Aggregate_Discrepant_Information/links/5beb143d299bf1124fd0dc66/Uncertainty-Visualization-Influences-how-Humans-Aggregate-Discrepant-Information.pdf)." From the paper: "Our study repeatedly presented two [GPS] sensor measurements with varying degrees of inconsistency to participants who indicated their best guess of the “true” value. We found that uncertainty information improves users’ estimates, especially if sensors differ largely in their associated variability". 


<!-- /wp:paragraph -->

<!-- wp:image {"align":"right","width":288,"height":191} -->
<div class="wp-block-image"><figure class="alignright is-resized"><img src="http://e.huffpost.com/pollster/share/2016-general-election-trump-vs-clinton.png?1490979763" alt="Image result for clinton trump polls" width="288" height="191"><figcaption>Source <a href="https://elections.huffingtonpost.com/pollster/2016-general-election-trump-vs-clinton">HuffPost</a></figcaption></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
Also recall the surprise when Donald Trump won the presidential elections despite the fact that most of the polls predicted that Hillary Clinton had higher chances to win. Nobody cared about uncertainty, everyone saw the graphs!


<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
### Why not error bars?


<!-- /wp:heading -->

<!-- wp:paragraph -->
Keep in mind that error bars are considered harmful, and I have a [reference to support this claim](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6214189/). But why? 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
First of all, error bars tend to be symmetric (although they don't have to) which might lead to the situation that we saw in the first example above: implying illegal values. 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Secondly, error bars are "rigid", implying that there is a certain hard threshold. Sometimes the threshold indeed exists, for example a threshold of H0 rejection. But most of the time, it doesn't.


<!-- /wp:paragraph -->

<!-- wp:image {"align":"right","width":234,"height":155} -->
<div class="wp-block-image"><figure class="alignright is-resized"><img src="https://images.unsplash.com/photo-1534951009808-766178b47a4f?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=crop&amp;w=1000&amp;q=80" alt="stacked round gold-colored coins on white surface" width="234" height="155"></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
More specifically to bar plots, error lines break the bar analogy and  are hard to read. First, let me explain the "bar analogy" part.


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
The thing with bar charts is that they are meant to represent physical bars. A physical bar doesn't have soft edges and adding error lines simply breaks the visual analogy.


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Another problem is that the upper part of the error line is more visible to the eye than the lower one, the one that is seen inside the physical bar. See?![undefined](/assets/img/2019/10/screen-shot-2019-10-07-at-9.09.06.png){:width=""}


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
But that's not all. The width of the error bars separates the error lines and makes the comparison even harder. Compare the readability of error lines in the two examples below


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
![](/assets/img/2019/10/image-1.png){:width=""} ![](/assets/img/2019/10/image-2.png){:width=""}


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
The proximity of the error lines in the second example (take from [this site](https://andrewpwheeler.wordpress.com/2016/03/08/on-overlapping-error-bars-in-charts/)) makes the comparison easier.


<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
### Are there better alternatives?


<!-- /wp:heading -->

<!-- wp:paragraph -->
Yes. First, I recommend reading the "Error bars considered harmful" paper that I already mentioned above. It not only explains why, but also surveys several alternatives


<!-- /wp:paragraph -->

<!-- wp:image {"id":2665,"sizeSlug":"large"} -->
<figure class="wp-block-image size-large"><img src="/assets/img/2019/10/image-5.png" alt="" class="wp-image-2665"></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
Nathan Yau from flowingdata.com had an[ extensive post about different ways to visualize uncertainty](https://flowingdata.com/2018/01/08/visualizing-the-uncertainty-in-data/). He reviewed ranges, shades, rectangles, spaghetti charts and more. 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Claus Wilke's book "[Fundamentals of Data Visualization"](https://amzn.to/2MhxFna) has a dedicated chapter to uncertainty with and even more detailed review [[link](https://serialmentor.com/dataviz/visualizing-uncertainty.html)].


<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":2662,"width":207,"height":267,"sizeSlug":"large","linkDestination":"custom"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://amzn.to/2MhxFna"><img src="/assets/img/2019/10/image-4.png" alt="" class="wp-image-2662" width="207" height="267"></a></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
"[Visualize uncertainty about the future](https://pdfs.semanticscholar.org/7aa9/0fc8be156d120f4740c68db8a191083f2a34.pdf?_ga=2.185789230.626538444.1570430727-825569699.1570430727)"  is a Science article that deals specifically with forecasts


<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":2668,"width":284,"height":258,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="/assets/img/2019/10/image-6.png" alt="" class="wp-image-2668" width="284" height="258"></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
Robert Kosara from Tableu experimented with [visualizing uncertainty in parallel coordinates](https://kosara.net/papers/2012/Dasgupta-EuroVis-2012.pdf).


<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":2669,"width":329,"height":194,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="/assets/img/2019/10/image-7.png" alt="" class="wp-image-2669" width="329" height="194"></figure></div>


<!-- /wp:image -->

<!-- wp:paragraph -->
There are many more examples and experiments, but I think that I will stop right now.


<!-- /wp:paragraph -->

<!-- wp:heading -->
## The bottom line


<!-- /wp:heading -->

<!-- wp:paragraph -->
Communicating uncertainty is important. 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Know your tools.


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Try avoiding error bars. 


<!-- /wp:paragraph -->

<!-- wp:paragraph -->
Bars and bars don't combine well, therefore, try harder avoiding error bars in bar charts.


<!-- /wp:paragraph -->
