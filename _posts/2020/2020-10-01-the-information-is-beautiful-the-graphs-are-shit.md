---
layout: post
title: "The information is beautiful. The graphs are shit!"
date: 2020-10-01
categories: 
  - "blog"
tags: 
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "worst-practice"
coverImage: "/assets/images/2020/10/featured_image.017.jpeg"
---

I apologize for my harsh language, but recently I was exposed to a bunch of graphs on the "information is beautiful" site, and I was offended (well, ot really, but let's pretend I was). I mean, I'm a liberal person, and I don't care what graphs people do in their own time. Many people visit that site because they try to learn good visualization practices, but some charts on that site are wrong. Very wrong.

Here's the gem:  

![](/assets/images/2020/10/image.png?w=1024)

I deliberately don't share the link to this site. I don't want let Google think it's valuable in any way.

Now, the geniuses from "Information is beautiful" (let's call them IB for brevety) wanted to share with us some positive stats. How nice of them. So what they did? They gathered together nine pairs of metrics collected at two different time points: one in the past and one furthermore in history. They used nice colors to create some sleeky shapes. So, what's the problem? What's wrong with that?

## Everything is wrong!

Let's start from my guess that they cherry-picked the stats with "positive" changes. Secondly, the comparison of this sort is mostly meaningless if we compare points at different years. What stopped the authors of that tasteless "infographic" from collecting data from the same years? I guess, their laziness. That's how we ended up comparing the number of death penalties in 1990 and 2016, but the malaria deaths numbers are for 2000 and 2016, and dying mothers are compared for years 2000 and 2017?

### Now, let's talk about data viz.

Take a look at this graph.

![](/assets/images/2020/10/image-1.png?w=879)

The only time we use shapes like that is when we want to convey information about uncertainty. To do that, the X-axis represents the thing we are measuring, and the Y-axis represents our certainty about the current value. When we compare to uncertain measurements, we may judge the difference between these measurements by the distance between the curve peaks, and the width of the curve represents the uncertainty.

Here's a good example from \[[this link](https://vwo.com/why-us/technology/bayesian-statistics/)\]:

![](/assets/images/2020/10/image-2.png?w=1024)

Can you see how the metric of interest is on the X-axis? The width of each bell curve represents the uncertainty and the difference between any pair of cases is the difference on the **horizontal (X) axis**, not the vertical one.

Instead, what do the IB authors did? They obviously like sleek looking shapes but know nothing about how to use them. They could have used two bars and let the viewer compare their heights. But nooooo! Bars are not c3wl! Bars are boring! Instead, they took probability density curves (that's how they are technically called) and made them pretend to be bars.

<figure>

![](/assets/images/2020/10/after.png?w=129)

<figcaption>

Bars. Is this THAT hard?

</figcaption>

</figure>

I can hear some of you saying, "Stop being so purist! What's wrong with comparing the heights of bell curves?" I'll tell you what's wrong! Data visualization is a language. As with any language, it has some rules and traditions. If you hear me saying, "me go home," you will understand me without any problem. However, you will silently judge me for my poor use of the English language. I know that, and since English is my third language, I use all the help to make as few mistakes as possible. The same is correct with data visualization. Please respect its rules and traditions, even if (and especially if) are not fluent in it.

<figure>

![](/assets/images/2020/10/image-3.png?w=1024)

<figcaption>

I never write more than two sentences in English without Grammarly

</figcaption>

</figure>

Visit the [worst practice tag](https://gorelik.net/tag/worst-practice/) in this blog to see more bad examples
