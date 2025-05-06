---
layout: post
title: "On algorithmic fairness &amp; transparency"
date: 2018-02-28
categories: 
  - "blog"
tags: 
  - "algorithms"
  - "bias"
  - "data-science"
  - "diversity"
  - "fairness"
  - "inclusion"
  - "machine-learning"
coverImage: "/assets/images/2018/02/justice.jpeg"
---

My teammate, [Charles Earl](https://charlesearl.blog) has recently attended the [Conference on Fairness, Accountability, and](https://fatconference.org/) [Transparency (FAT\*)](https://fatconference.org/). The conference site is full of very interesting material, including proceedings and video recording of lectures and tutorials.

Reading through the conference proceedings, I found a very interesting paper titled "[The Cost of Fairness in Binary Classification](http://proceedings.mlr.press/v81/menon18a/menon18a.pdf)." This paper talks about the measures one needs to take in order not use sensitive features (such as race) as the means to discrimination, with a reasonable accuracy tradeoff.

Skimming through this paper, I recalled a conversation I had about a year ago with a chief data scientist in a startup that provides short-term loans to people who need some money **now**. The major job of the data science team in that company was to assess the risk of a customer. From the explanation the chief data scientist gave, and from the data sources she described, it was clear that they train their model on the information whether a person is likely to receive a loan from a financial institution. When I pointed out that they exclude categories of people that are rejected but are likely to return the money. "Yes?" she said in a tone as if she couldn't see what the problem that I tried to raise was. "Well," I said, it's unfair for many customers, plus you're missing the chance to recruit customers who were rejected by others". "We have enough potential customers," she said. She didn't think fairness was an issue worth talking about.

 

The featured image is by [Søren Astrup Jørgensen from Unsplash](https://unsplash.com/photos/oux1EInHTM4)
