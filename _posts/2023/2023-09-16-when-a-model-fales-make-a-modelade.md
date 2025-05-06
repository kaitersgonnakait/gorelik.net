---
layout: post
title: "When a Model Fales, Make a Modelade"
date: 2023-09-16
categories: 
  - "blog"
  - "direction-matters"
coverImage: "/assets/images/2023/09/screenshot-2023-09-16-at-19.49.59.png"
---

Or, How to Extract Value from Failed Projects

Typically, a professional post should begin with an introductory paragraph that provides some background and engages the reader. Let’s pretend that such a paragraph has been written and proceed directly to the story at hand. This story doesn't end happily, nor does it end sadly. It simply begins and ends, and that's all. Nonetheless, it's worth your time.

## The Story

I have a client who implements a variety of smart algorithms to assist individuals with money and innovative ideas in making a positive impact on society and the environment. They requested my help with modeling, and given my extensive experience as a data scientist and my track record of building numerous predictive models, I was keen to assist.

After working our modeling magic, we ended up with a predictive model that was "statistically significant" but practically unusable. What do I mean by that? Typically, we evaluate the value of a predictive model by comparing the predicted values with the known ("observed") ones. Standard comparison procedures involve a correlation metric (or R-squared, which is NOT a correlation metric) and, for those who want to sound intellectual, a p-value. Both these metrics were excellent in our model. We also generated plots for a more comprehensive analysis. Below is a representation of our data using a completely fictitious dataset (rest assured, I would never share a client's data).

## Statistically Significant but Practically Useless

The graph indeed looks promising: the correlation coefficient was over 0.95, and the p-value (I can't believe I'm resorting to this!) was 0.00000001, which is considered "excellent." 

However, there's the rub: echoing an old Russian proverb, "you can't spread the p-value on your bread", or to quote a less old Hebrew saying, "you can't pay with a correlation coefficient at the grocery store." Statistical tests demonstrate the existence of a connection between your model and reality. Yet, this connection isn't sufficient for making informed decisions due to the excessively high spread in our case.

For our model to be of practical use to my client's clients, the typical deviation from real life should be within an order of magnitude of 0.5 (whatever the units may be). If the deviation is higher, my client's clients would be wasting time and money. Despite our diligent efforts and the extensive work with the client's team, the typical deviation was significantly larger, rendering the model practically useless.

## … or is it?

An old Yiddish adage offers wisdom: \[yeah, I don't have anything relevant, but I'm sure there is one\]. Consider our situation: we've spent considerable time and effort building a model. Does the model's prediction bear any relation to reality? Yes. Are the deviations too high? Again, yes. What does this mean? It indicates that many instances we're trying to model don't behave as anticipated based on our data. Herein lies an opportunity.

In this project, we're attempting to forecast a key business metric. If an entity's metrics are notably worse than expected, this identifies a significant opportunity for improvement—a low-hanging fruit. Consequently, my client or my client's clients could approach the entity and offer assistance.

However, there's another side to this. What hasn't been mentioned is that the "observed" data comes from self-reports. This implies that some reports may be manipulated to portray a more optimistic picture than reality. Therefore, the same model can be used to identify potential "mistakes" 😉 in self-reports, which is a valuable exercise in its own right.

## A happy ending?

The typical "war story" of a freelance consultant generally concludes with the client accepting the consultant's insights, raking in substantial profits, and treating the consultant to a swanky race car. Let's pretend that this is what happened, despite the reality: my client listened to my take and decided to invest their resources in procuring more high-quality data. 

Of course, if you ever need help with your modeling, feel free to reach out to me. And if a model doesn't turn out as productive as you'd hoped, we can always attempt to make a rewarding 'modelade' from it. I'm always reachable at boris@gorelik.net.
