---
layout: post
title: "What is the biggest problem of the Jet and Rainbow color maps, and why is it not as evil as I thought?"
date: 2020-08-17
categories: 
  - "blog"
tags: 
  - "colormap"
  - "colors"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
  - "jet"
  - "turbo"
coverImage: "/assets/images/2020/08/featured_image.013.jpeg"
---

There was a consensus among the data visualization purists that the rainbow color map, and it's close cousin Jet are bad. Really bad. These colormaps used to be popular at the beginning of the computational data visualization era. However, their popularity decreased in the last five years or so. The sentiment isn't as bad as it used to be a couple of years ago, but still.

<figure>

![](/assets/images/2020/08/image.png?w=1024)

<figcaption>

A screenshot from circa 2016. Today we are less fanatic than that

</figcaption>

</figure>

What is the biggest problem of the rainbow colormap? The most apparent problem with this particular colormap is that it not perceptually uniform. By "perceptually uniform," I mean that equal changes in the value that we encode using a colormap should correspond to same changes in the color perception. This is not the case with the rainbow or the Jet colormaps. They have distinct bright and dark stripes within the number range, making them the wrong choice to encode numerical data. The situation is even worse for people with impaired color vision.

<figure>

![](/assets/images/2020/08/image-1.png?w=1024)

<figcaption>

Can you be less perceptually uniform?

</figcaption>

</figure>

The solution to this problem was proposed in the form of better colormaps. The first one that I know of is [Parula by Matlab](https://www.mathworks.com/help/matlab/ref/parula.html), and it's opensource alternative Viridis that is available in matplotlib and many other plotting libraries. (Watch [this video about viridis](https://www.youtube.com/watch?v=xAoljeRJ3lU) to get a good introduction to color perception and color maps).

<figure>

![](/assets/images/2020/08/image-2.png?w=1024)

<figcaption>

Viridis, the new rainbow

</figcaption>

</figure>

Everything was nice and good, and I was trashing the rainbow colormap whenever I could. Until yesterday, when I read about Turbo, the improved rainbow colormap developed by Google.

In the [long and interesting blog post that describes Turbo](https://ai.googleblog.com/2019/08/turbo-improved-rainbow-colormap-for.html), Anton Mikhailov, a software engineer in Google, describes several relevant applications of a "good rainbow" scheme. 

![](/assets/images/2020/08/image-3.png?w=1000)

According to Anton, "Because of rapid color and lightness changes, Jet accentuates detail in the background that is less apparent with Viridis and even Inferno. Depending on the data, some detail may be lost entirely to the naked eye. The background in the following images is barely distinguishable with Inferno (which is already punchier than Viridis), but clear with Turbo."

I must admit that I'm convinced. 

The biggest problem with that is mentioned concerning the original rainbow scheme that its brightness varies too much. However, it turns out that the color saturation and hue attract our attention more than the lightness (here's the [reference](https://onlinelibrary.wiley.com/doi/abs/10.1002/col.10214) which I haven't read yet). As such, it makes sense to construct a colormap that relies more on color and hue changes. 

Moreover, in many cases, the interesting details appear in the extreme values of the data range, not in the middle. In thes cases, a properly applied rainbow-like color scheme becomes a valid choice.

![](/assets/images/2020/08/image-4.png?w=1024)

The bottom line is that one should not refrain from using rainbow(-like) color maps in their visualizations anymore, provided that they use a modern implementation. Luckily, it's even available in matplotlib
