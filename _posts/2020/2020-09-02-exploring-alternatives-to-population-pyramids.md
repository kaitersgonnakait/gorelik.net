---
layout: post
title: "Exploring alternatives to population pyramids"
date: 2020-09-02
categories: 
  - "blog"
tags: 
  - "age-pyramid"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
coverImage: "/assets/images/2020/09/featured_image.015.jpeg"
---

A population pyramid also called an "age-gender-pyramid", is a graphical illustration that shows the distribution of various age groups in a population (typically that of a country or region of the world), which forms the shape of a pyramid when the population is growing \[citation from [Wikipedia](https://en.wikipedia.org/wiki/Population_pyramid)\].

In some cases, the pyramid provides interesting insights into the entire population. In this post, I will explore ways to make some of these insights more visible. 

## The basic case

Let's start with the basic case. If you have two-three hours of spare time, you can go to the site devoted to population pyramids -- https://www.populationpyramid.net. There, you will find population pyramids for every country in the world. The site provides present and past data, as well as future forecasts. To understand how insightful age pyramids can be, look at the graph that represents the entire world.

![](/assets/images/2020/09/image-1.png?w=862)

(this and most other images in this post are from the site http://populationpyramid.net/)

You can clearly see that the world is mostly young, that the amount of people declines as the age progresses, and that there is a rough balance between men and women in the world, at least before the ages of 70+.

Now, examine the stark difference between the populations of Western Africa and Western Europe. Citing the late professor Hans Rosling, we can still see two worlds, one with large families and short lives, and one with small families and long lives. 

![](/assets/images/2020/09/image-2.png?w=936)

Another starking example of an age pyramid is the following

![](/assets/images/2020/09/image-3.png?w=862)

Do you want to guess what country is that? This particular graph shows the age distribution of the United Arab Emirates. Such a vast distortion in symmetry and age distribution stems from the fact that more than 80% of the UAE's population is composed of expats who come to this rich country to work. The pyramid below (taken from \[[this article](https://www.sciencedirect.com/science/article/pii/S2210600612000214)\]) sheds some light to the population composition of UAE. (Note that the genders in this graph are reversed).

![](/assets/images/2020/09/image-3.jpeg?w=548)

## Whose bar is longer?

The male-female disbalance in the UAE and some other Gulf countries is very striking and cannot be missed. But what about other, more subtle cases? Take a look at the world graph above. If you follow the numbers on the bars, you will notice that more boys are born than girls, but there are more old ladies than old gents in the world. Can we make such differences less subtle?

To answer this question, we need to understand why we find it hard to compare almost equal bars. The reason for that is that our eyes (or brains) are not so good at comparing sizes. They do, however, do a much better job comparing positions. Thus, if we overlap these bars, we will see the small differences in a much more precise manner. 

![](/assets/images/2020/09/image-4.jpeg?w=676)

(I thank the data visualization expert [Bella Graf](https://www.facebook.com/bella.gotie) from [InfoServiz.co.il](https://infoserviz.co.il/) for the idea of this graph).

Now, the subtle differences in gender composition are more visible. 

## What am I looking at?

When I teach data visualization, I always tell my students to add a meaningful title to the graph. By "meaningful," I mean a title that does not answer the question "what" but rather "so what"? (See my posts "[How to suck less in data visualization](https://gorelik.net/2020/07/28/how-to-suck-less-in-data-visualization-and-professional-communication/)," and "[C for conclusion](https://gorelik.net/2018/06/25/c-for-conclusion/)"). What would a good title for this graph be? Let's try the following

![](/assets/images/2020/09/image-5.jpeg?w=676)

OK, so now, when we have a title, we can ask ourselves, "does the graph show what it says it shows"? And the answer is no. Right now, the title talks about differences, but we don't see the differences. We see the differences and other stuff. Let's look only at the differences.

![](/assets/images/2020/09/image-6.jpeg?w=676)

I don't like this.

What about this?

![](/assets/images/2020/09/image-8.png?w=874)

Now, this is not an age pyramid. That's for sure. This graph doesn't show the wealth of data that the classical pyramid shows. On the other hand, it does offer one thing, and it does it very well. Look, for example, at the male/female distortion in China in 1990.

![](/assets/images/2020/09/image-9.png?w=866)

You may find the code I used to create the graphs in this post \[[on GitHub](http://github.com/bgbg/blog_exploring_age_pyramics)\].
