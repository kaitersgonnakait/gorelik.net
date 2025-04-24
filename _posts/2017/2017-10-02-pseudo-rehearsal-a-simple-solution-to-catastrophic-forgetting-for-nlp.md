---
layout: post
title: "Pseudo-rehearsal: A simple solution to catastrophic forgetting for NLP"
date: 2017-10-02
categories: 
  - "blog"
tags: 
  - "machine-learning"
coverImage: "/assets/images/2017/10/void.jpg"
---

Frequently, training a machine learning model in a single session is impossible. Most commonly, this happens when one needs to update a model with newly obtained observations. The generic term for such an update is "online learning." In the scikit-learn world, this concept is also known as partial fit.  The problem is that some models or their implementations don't allow for partial fit. Even if the partial fitting is technically possible, the weight assigned to the new observations is may not be under your control. What happens when you re-train a model from scratch, or when the new observations are assigned too high weights? Recently, I stumbled upon an interesting concept of Pseudo-rehearsal that addresses this problem. Citing [Matthew Honnibal](https://explosion.ai/blog/pseudo-rehearsal-catastrophic-forgettinghttps://explosion.ai/blog/pseudo-rehearsal-catastrophic-forgetting):

> Sometimes you want to fine-tune a pre-trained model to add a new label or correct some specific errors. This can introduce the "catastrophic forgetting" problem. Pseudo-rehearsal is a good solution: use the original model to label examples, and mix them through your fine-tuning updates.

This post is written by Matthew Honnibal from the team behind the excellent [Spacy NLP library.](https://spacy.io/) This post is valuable in many aspects. First, it demonstrates a simple-to-implement technique. More importantly, it provides the [True Name](https://en.wikipedia.org/wiki/True_name) for a problem I encounter from time to time: [Catastrophic forgetting](https://scholar.google.co.il/scholar?hl=en&q=catastrophic+forgetting&btnG=&as_sdt=1%2C5&as_sdtp=).

 

Featured [image](https://www.flickr.com/photos/herrolsen/5388521148/in/photolist-9dazB3-saPn4G-dm3Cvs-3N4e4d-7fmo8b-7fhxVV-7fhoPn-7fmpEy-7KRJAg-7fhoHZ-5YWLwy-dm3Awt-c8A9iN-7Wp5ej-c6GQfu-YashAr-xKTD9v-7fhySe-7fmqTw-3kdDn-4pj8fj-7fmrmW-dm3DDb-dm3DZh-4FXUjB-7fhwai-6gR4Jn-7fmsr9-7fmqZ7-C9BDrT-cRgK2-j61DKu-mRDqJp-2PhywT-7fmrGh-7fhyjM-jT9Npx-7pUCQT-pZDiG-7fhypp-7fmruJ-adkwq1-jmGDVa-6BsxLw-dcGQza-6VDu3i-7fhyEe-ebNqo1-pZDmc-bUvX2o) is by Flickr user Herr Olsen under CC-by-nc-2.0
