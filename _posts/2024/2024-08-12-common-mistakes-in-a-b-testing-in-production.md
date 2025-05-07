---
title: "Common mistakes in A/B testing in production"
date: 2024-08-12
categories: 
 - "blog"
layout: "post"
---

I performed my first A/B tests ten years ago. Here are the most common mistakes I made

1. Doing an A/B test in the first place

   Yes, the first mistake is doing the A/B test in the first place. An A/B test is an experiment. Many changes in products or services are not part of an experiment. They can be driven by business decisions, tech limitations, or shifting values. In these cases, managers decide to perform A/B tests to ease their conscience. This dilutes the concept of testing. A better approach is gradual deployment and post-deployment monitoring.

2. Not comparing apples to apples

   Sometimes, especially in organizations new to A/B testing, the “B” variant is deployed using a workaround or a hack. In one case I witnessed during my freelancing career, the “B” variant was created by injecting pieces of JavaScript into the frontend, causing it to malfunction on several browsers. In another case, the test algorithm was deployed on an old and slow server. In both cases, the diminished performance of the “B” variant wasn’t because it was inherently worse but because of these implementation issues.

3. Not defining proper metrics

   What do you want to measure? Conversion, lifetime value, user satisfaction? Do you assign the same weight to an improvement in one metric compared to a decrease in another? How sensitive are you to the risk of adopting the “B” variant when it’s actually worse? What about the opposite scenario? Answering these questions is critical. It’s the data person’s responsibility to ask them and demand answers. It’s the leadership’s responsibility to provide meaningful and thoughtful responses.

4. Not committing beforehand

   Before starting an A/B test, discuss all possible outcomes and commit to accepting them. If you ignore some types of outcomes, you don’t need to perform the test at all (see point **#1**).

5. The peeking problem

   I’ve seen many test owners examine the results of ongoing tests and decide whether to continue based on what they see. This is called peeking. Depending on the statistical approach you use, peeking ranges from being frowned upon to a huge no-no. If you can’t resist peeking, I advise using Bayesian methods for analysis which are considered less prone to errors from peeking.

6. Relying too much on statistical tests

   You might recall power analysis from your introductory stats classes. We use power analysis to define the experiment size. Too small a sample size, and you won’t detect meaningful differences; too large, and you may waste resources. But sometimes, sample size isn’t the whole story. Some sites and applications have such high traffic that you can reach the required sample size in hours or days. However, if you do so, you might miss intrinsic variations in audience behavior: your nighttime users might differ from your daytime users, and weekday interactions may differ from weekend ones. Ignoring these aspects in your test planning can lead to unpleasant surprises.
