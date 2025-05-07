---
title: "How to make a graph less readable? Rotate the text labels"
date: 2017-11-23
categories: 
 - "blog"
tags: 
 - "because-you-can"
 - "best-practice"
 - "data-visualization"
 - "dataviz"
cover_image: "/assets/img/2017/11/head-tilting-dog.jpg"
layout: "post"
---

This is my "[because you can](https://gorelik.net/tag/because-you-can/)" rant.

Here, you can see a typical situation. You have some sales data that you want to represent using a bar plot.

![01_default](/assets/img/2017/11/01_default.png){:width="432" :class="alignnone"}

Immediately, you notice a problem: the names on the X axis are not readable. One way to make the labels readable is to enlarge the graph.![02_large_image](/assets/img/2017/11/02_large_image.png){:width="1296" :class="alignnone"}

Making larger graphs isn't always possible. So, the next default solution is to rotate the text labels.

![03_rotated](/assets/img/2017/11/03_rotated1.png){:width="864" :class="alignnone"}

However, there is a problem. Rotated text is read more slowly than standard horizontal text. Don't believe me? This is not an opinion but rather a result of empirical studies [[ref](http://journals.sagepub.com/doi/abs/10.1177/154193120204601722)], [[ref](http://psycnet.apa.org/record/1986-10970-001)]. Sometimes, rotated text is unavoidable. Most of the time, it is not.

So, how do we make sure all the labels are readable without rotating them? One option is to move them up and down so that they don't hinder each other. It is easily obtained with Python's matplotlib

[code language="python"]
plt.bar(range(len(people)), sales)
plt.title('October sales')
plt.ylabel('$US', rotation=0, ha='right')
ticks_and_labels = plt.xticks(range(len(people)), people, rotation=0)
for i, label in enumerate(ticks_and_labels[1]):
    label.set_y(label.get_position()[1]  (i % 2) * 0.05)
[/code]

(note, that I also rotated the Y axis label, for even more readability)

![05_alternate_labels](/assets/img/2017/11/05_alternate_labels.png){:width="864" :class="alignnone"}

Another approach that will work with even longer labels and that requires fewer code lines it to rotate the bars, not the labels.

![07_horizontal_plot](/assets/img/2017/11/07_horizontal_plot.png){:width="864" :class="alignnone"}

... and if you don't have a compelling reason for the data order, you might also consider sorting the bars. Doing so will not only make it prettier, it will also make it easier to compare between similar values. Use the graph above to tell whether Teresa Jackson's sales were higher or lower than those of Marie Richardson's. Now do the same comparison using the graph below.

![08_horizontal_plot_sorted](/assets/img/2017/11/08_horizontal_plot_sorted.png){:width="864" :class="alignnone"}

To sum up: the fact you can does not mean you should. Sometimes, rotating text labels is the easiest solution. The additional effort needed to decipher the graph is the price your audience pays for your laziness. They might as well skip your graphs your message won't stick.

This was my [because you can](https://gorelik.net/tag/because-you-can/) rant.

<small>Featured image by <a href="https://www.flickr.com/photos/gullevek/219632672/in/photolist-kpF9d-bE7Np2-bE7Noi-brcR9m-bE7jjF-bE7nAv-bE7S6i-bE7jFx-bE7TLV-bE7VVB-bE7NoR-brcJZW-bE7sLp-brcnWA-m9yjcH-bE7TMc-bE7VVz-bE7iqz-bE824D-7Bcw3w-bE824v-bE7mND-bE7S6a-brcK19-brcR9s-7vEsMC-bE7Not-brcJZS-bE7jBH-qD2axf-bE7NoB-bE7TMx-brcR9y-brcnQU-bE7TMp-bE824H-brd3ww-brcR9G-4DqSRG-4TbPtZ-brd3vY-bE7Npi-bE7ms6-bE7jhz-bE7S5F-bE7AWx-bE7TMT-bE7S6p-bE7TMH-bE7VW8" target="_blank" rel="noopener">Flickr user gullevek</a></small>
