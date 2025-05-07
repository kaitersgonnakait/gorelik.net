---
title: "Why is it (almost) impossible to set deadlines for data science projects?"
date: 2017-10-19
categories: 
 - "blog"
tags: 
 - "complexity"
 - "data-science"
 - "problem"
 - "project-management"
cover_image: "/assets/img/2017/10/gantt.png"
layout: "post"
---

In many cases, attempts to set a deadline to a data science project result in a complete fiasco. Why is that? Why, in many software projects, managers can have a reasonable time estimate for the completion but in most data science projects they can't? The key points to answer this question are complexity and, to a greater extent, missing information. By "complexity" I don't (only) mean the computational complexity. By "missing information" I don't mean dirty data. Let us take a look at these two factors, one by one.

## Complexity

![Illustration: famous xkcd comic. Two programmers play during the compilation time](/assets/img/2017/10/compiling.png){:width="300"}
Think of this. Why most properly built bridges remain functional for decades and sometimes for centuries, while the rule in every non-trivial program is that "there is always another bug?". I read this analogy in Joel Spolsky's [post written in 2001](https://www.joelonsoftware.com/2001/12/). The answer Joel provides is:

> Once you’ve written a subroutine, you can call it as often as you want. This means that almost everything we do as software developers is something that has never been done before. This is very different than what construction workers do.


There was a substantial progress in the computer engineering theory since 2001 when Joel wrote its post. We have better static analysis tools, better coverage tools, and better standard practices. Nevertheless, bug-free software only exists in Programming 101 books.

What about data science projects? Aren't they essentially a sort of software project? Yes, they are, and as such, the above quote is relevant for them too. However, we can add another statement:

> Once you’ve collected data, you can process it as often as you want. This means that almost everything we do as data scientists is something that has never been done before.


You see, to account for project uncertainty, we need to multiply the number of uncertainty factors of a software project by the number of uncertainty factors associated with the data itself. The bottom line is an exponential complexity growth.

## Missing information

Now, let's talk about another, even bigger problem, the missing information. I'm not talking about "dirty data" -- a situation where some values in the dataset are missing, input errors, or fields that change their meaning over the time. These are severe problems but not as tough as the problem I'm about to talk about in this post.

When a software engineer writes a plotting program, they know when it doesn't work: the image is either created or not. And if the image isn't created, the programmer knows that something wrong and has to be fixed. When a programmer writes a compression program, they know when they made a mistake: if the program does not compress a file, or if the result isn't readable. The programmer knows that there must be a fixable bug in his or her code.

What about a data science project? Let's say you're starting an advertisement targetting project. The project manager gives you the information source and the performance metric. A successful model has to have a performance of 80 or more (the nature of the performance score isn't important here). You start working. You clean your data, normalize it, build a nice decision tree, and get a score of 60, which is way too low. You explore your data, discover problems in it, retrain the tree and get 63. You talk to the team that collects the data, find more problems, build a random forest, train it and get a score of 66. You buy some computation time, create a deep learning network on AWS, train it for a week, and get 66 again.

![Illustration: a blindfolded man wandering around](/assets/img/2017/10/387313596_e0ef59f7bd_z.jpg){:width="200"}

What do you do now? Is it possible that somewhere in your code there is a bug? It certainly is. Is it possible that you can improve the performance by deploying a better model? Probably. However, it is also possible that the data does not contain enough information. The problem, of course, is that you don't know that. In practice, you hit your head against the wall until you get the results, or give up, or fired. And this is THE most significant problem with data science (and any research) project: your problem is a black box. You only know what you know, but you have no idea what you don't. A research project is like exploring a forest with your eyes shut: when you hit a tree, you don't know whether this is the last tree in the forest and you're out, or you're in the middle of a tropical jungle.

I hope that the theoretical data science research will narrow this gap. Meanwhile, the project managers will have to live with this great degree of uncertainty.

 

PS. As in any opinion post, I may be mistaken. If you think I am, please let me know in the comments section below.

<small>The xckd image: https://xkcd.com/303/ under CC-nc. The wandering man image: Illustration: a blindfolded man wandering around. By <a href="https://www.flickr.com/photos/moominmolly/387313596/in/photolist-Ae5QC-dSNMiE-5M2J6B-FUxM3-AjunK-AjunQ-FTekM-7ZHpSg-8kSzar-8ixvSk-FS21G-d3S2m-9HwsZ-FUCHX-dqiKX9-4RRqpp-4vDDzP-67uoV3-2sxeW-46iQs-6p73Ux-SCkuC2-FS4VP-4crvCj-FS6pr-63FdXT-3Mv5CA-5hfAQi-9VV3mh-7G252-nm2Vob-cRyGwd-6Pf8zW-bmS8su-dBtXLu-SL5fu1-9z6YG9-4cg9xS-Vziu3x-Bhet8q-nvTi9a-tV7Fv-6PawCA-6PdYW9-J8R4zo-G3YF6q-JDoTHY-gwmAC2-k9iixX-fqHdVc">Flickr user Molly</a> under CC-by-nc-nd
</small>
