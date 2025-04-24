---
layout: post
title: "Before and after — the Hebrew holiday season chart"
date: 2017-10-08
categories: 
  - "blog"
tags: 
  - "before-after"
  - "data-visualization"
  - "dataviz"
coverImage: "/assets/images/2017/10/tishrei_workign_days_before_and_after2.png"
---

Sometimes, when I see a graph, I think "I could draw a better version." From time to time, I even consider writing a blog post with the "before" and "after" versions of the plot. Last time I had this desire was when I read the repost of my own [post about the crazy month of Hebrew holidays](http://gorelik.net/2017/09/27/16-days-work-month-the-joys-of-the-hebrew-calendar-2/). I created this graph three years ago. Since then, I have learned A LOT. So I thought it would be a good opportunity to apply my over-criticism to my own work. This is the "before" version:

![Graph: Tishrei is mostly a non-working month.](/assets/images/2017/10/tishrei_workign_weeks.png)

There are quite a few points worth fixing in that plot. Let's review those problems:

- The point of the original post is to emphasize the amount of NON-working days in Tishrei. However, the largest points represent the working days. As the result, the emphasis goes to the working days, thus reversing the semantics.
- It is not absolutely clear what point I intended to make using this graph. A short and meaningful title is an effective way to lead the audience towards the desired conclusion.
- There are three distinct colors in my graph, representing working, half-working and non-working days. The category order is clear. The color order, on the other hand, is absolutely arbitrary. Moreover, green and red are never a good color combination due to the significantly high prevalence of impaired color vision.
- Y label is rotated. Rotated Y labels are the default option in all the plotting tools that I know. Why is that is beyond my understanding, given the numerous studies that show that reading rotated text takes more time and is more error-prone (for example, see [ref](http://journals.sagepub.com/doi/abs/10.1177/154193120204601722), [ref](http://jov.arvojournals.org/article.aspx?articleid=2121153), and [ref](http://psycnet.apa.org/record/1986-10970-001).)
- One interesting piece of information that one might expect to read from a graph is how many working days are there in year X. One can obtain this information either by counting the dots or by looking at a separate graph. It would be a good idea to make this information readily available to the observer.
- The frame around the plot is useless.

 

OK, now that we have identified the problems, let's fix them

- **Emphasize the right things.** I will use bigger points for the non-working days and small ones for the working days. I will also use squares instead of circles. Placing several squares one next to the other creates solid areas with less white space in-between. This lack of whitespace will help further emphasizing non-working chunks. I will make to leave _some_ whitespace between the points, to enable counting.
- **What's your point?** I will add an explanatory title. Having given some thought, I came up with "How productive can you be?". It is short, thought-provoking, and makes the point.
- **Reduce the number of colors.** My intention was to use red for non-working days, and blue for the working ones. What color should I use for the half-working ([Chol haMoed](https://en.wikipedia.org/wiki/Chol_HaMoed)) days? I don't want to introduce another color to the improved graph. Since in my case, those days are mostly non-working, I will use a shade of red for Chol haMoed.
- **Improve label readability.** One way to solve the rotated Y label problem is to remove the Y label at all! After all, most people will correctly assume that "2006", "2010", "2020" and other values represent the years. However, the original post mentions two different methods to count the years, using the Hebrew and Christian traditions. To make it absolutely clear that the graph talks about the Christian (common) calendar, I decided to keep the legend and format it properly.
- **Add more info.** I added the total number of working days as a separate column of properly aligned gray text labels. The gray color ensures that the labels don't compete with the graph.  I also highlighted the current year using a subtle background rectangle.
- **Data-ink ratio.** I removed the box around the graph and got rid of lines for the X and Y axes. I also removed the vertical grid lines. I wasn't sure about the horizontal ones but I decided to keep them in place.

This is the result:

![tishrei_working_days_after.png](/assets/images/2017/10/tishrei_working_days_after.png)

I like it very much. I'm sure though, that if I revisit it in a year or two, I will find more ways to make it even better.

You may find the code that generates this figure [here](https://gist.github.com/bgbg/1c91ff0eed54518157f5e74afab06603).
