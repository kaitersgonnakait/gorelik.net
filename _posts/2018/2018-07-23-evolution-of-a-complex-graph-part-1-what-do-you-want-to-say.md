---
layout: post
title: "Evolution of a complex graph. Part 1. What do you want to say?"
date: 2018-07-23
categories: 
  - "blog"
tags: 
  - "before-after"
  - "data"
  - "data-science"
  - "data-visualisation"
  - "data-visualization"
  - "dataviz"
coverImage: "/assets/images/2018/07/image006-fake-screenshot.png"
---

From time to time, people ask me for help with non-trivial data visualization tasks. A couple of weeks ago, a friend-of-a-friend-of-a-friend showed me a set of graphs with the following note:

Each row is a different use case. Each use case was tested on three separate occasions – columns 1,2,3. We hope to show that the lines in each row behave similarly, but that there are differences between the different rows.

Before looking at the graphs, note the last sentence in the above comment. Knowing what you want to show is an essential and not trivial part of a data visualization task. Specifying what is it **precisely** that you want to say is the first required task in any communication attempt, technical or not.

For the obvious reasons, I cannot share the original graphs that that person gave me. I managed to re-create the spirit of those graphs using a combination of randomly generated arrays. ![The original graph: A 3-by-4 panel of line charts](/assets/images/2018/07/image001-before.png) Notice how the X- and Y- axes are aligned between all the subplots. Such alignment is a smart move that provides a shared scale and allows faster and more natural comparison between the curves. You should always try aligning your axes. If aligning isn’t possible, make sure that it is absolutely, 100%, clear that the scales are different. Slight differences are very confusing.

There are several small things that we can do to improve this graph. First, the identical legends in every subplot are a useless waste of ink and thus, of your viewers' processing power. Since they are identical, these legends do nothing but distracting the viewer. Moreover, while I understand how a variable name such as `event_prob` appeared on a graph, showing such names outside technical teams is a bad practice. People who don’t share intimate knowledge with the underlying data will find human-readable labels easier to comprehend, making your message "stickier." Let’s improve the signal-to-noise ratio of this plot. ![An improved version of the 3-by-4 grid of line charts](/assets/images/2018/07/image002-improved-signal-to-noise.png)

According to our task, each row is a different use case. Notice that I accompanied each row with a human-readable label. I didn’t use cryptic code such as `group_001`, `age_0_10` or the such. Now, let’s go back to the task specification. “We hope to show that the lines in each row behave similarly, but that there are differences between the separate rows.” Remember my advice to [always use conclusions as graph titles](http://gorelik.net/2018/06/25/c-for-conclusion/)? Let’s test how such a title will look like

![A hypothetical screenshot. The title says: "low intra- & high inter- group variability"](/assets/images/2018/07/image003-hypothetic-screenshot.png)

Really? Is there a better way to justify the title? I claim that there is.

Let’s experiment a little bit. What will happen if we will plot all the lines on the same graph? By doing so, we might create a stronger emphasize of the similarities and the differences.

![Overlapping lines that show several repetitions in four different groups](/assets/images/2018/07/image004-overlapping-curves.png) Not bad. The separate lines create some excessive noise, and the legend [isn’t the best way to label multiple lines](http://gorelik.net/2017/04/12/chart-legends-and-the-muttonchops/), so let’s improve the graph even further.

![Curves representing four different data groups. Shaded areas represent inter-group variability](/assets/images/2018/07/image005-improved.png)

Note that meaningful ticks on the X-axis. The 30, 180, and 365-day marks provide useful anchors.

Now, let us go back to our title. “Low intra- and high inter- group variability” is, in fact, two conclusions. If you have ever read any text about technical presentations, you should remember the “one point per slide” rule. How do we solve this problem? In cases like these, I like to use the same graph in two different slides, one for each conclusion.

![Screenshot showing two slides. The first one is titled "low within-group variability". The second one is titled "High between-group variability". The graphs in the slides is the same](/assets/images/2018/07/image006-fake-screenshot.png)

During a presentation, I would show this graph with the first conclusion as a title. I would talk about the implications of that conclusion. Next, I will say "wait! There is more", will promote the slide and start talking about the second conclusion.

### To sum up,

First, decide what is it that you want to say. Then ask whether your graph says what you want to say. Next, emphasize what you want to say, and finally, say what you want to say.

### To be continued

The case that you see in this post is a relatively easy one because it only compares four groups. What will happen if you will need to compare six, sixteen or sixty groups? I will try answering this question in one of my next posts
