---
layout: post
title: "Mammogram, breast cancer, and manipulative statistics"
date: 2018-02-24
categories: 
  - "blog"
tags: 
  - "breast-cancer"
  - "mammogram"
  - "manipulation"
  - "probability"
  - "risk"
  - "statistics"
---

Here's a quiz

A healthy woman with no risk factors gets a positive mammogram result during a routine annual check. What is the probability that she actually has a breast cancer? Baseline data: The probability that a woman has breast cancer is 0.8%. If she has breast cancer, the probability that a mammogram will show a positive result is 90%. If a woman does not have breast cancer, the probability of a positive result is 7%.

Prof. Gerd Gigerenzer gave this quiz to numerous students, physicians, and professors. Most of them failed this quiz. The correct answer is 9%. The probability that a healthy woman has a breast cancer if she has a positive mammogram test is only nine percent! This means that ninety percent of women who get a positive result will undergo stressful and painful series of tests only to discover that that was a false alarm. In his book "[Calculated Risks](https://www.thriftbooks.com/w/calculated-risks-how-to-know-when-numbers-deceive-you_gerd-gigerenzer/322505/#isbn=0743205561)", prof. Gigerenzer uses this low probability as a starting (but not the only) argument against the common practice of routine population-wide mammogram tests. However, I would like to propose another way to look at this problem. To understand my concern, let me first explain how we get the 9% figure. There are several ways to get to this result. One of them is as follows. Eighty out of 10,000 women have breast cancer. Of those women, 72 (90% of 80) will test positive during a mammogram. Of the remaining 9,920 healthy women, about 694 (7%) will also have a positive mammogram test. The total number of women with a positive test is 766. Of those 766 women, only 72 have breast cancer, which is about 9%. The following diagram will help you track the numbers.

![Diagram that presents natural occurrence of breast cancer, and the statistics of mammogram tests](/assets/images/2018/02/mammogram_and_breast_cancer-e1519503231567.png)

Nine percent is indeed a low number. If a woman gets ten mammogram tests in her lifetime, there is a 60+% chance that she will have at least one false positive test. This is not something that can be easily ignored.

## However

Let's think about another way to look at this problem. Yes, the probability of a woman to have a breast cancer given that she has a positive mammogram result is nine percent (72 out of 697+72=766). However, the probability of a woman to have a breast cancer given that she has a **negative** mammogram result is 8 out of (9,223+8)=9,231 which is approximately 0.09%. That means that a woman with a positive mammogram test is 100 times more likely to have a breast cancer, compared to the woman with a negative result. Increase by a factor of 100 sounds like a serious threat. Much more serious than the nine percent! Moreover, a woman with a negative mammogram result knows that she is approximately ten times less likely to have a breast cancer than an average woman who didn't undergo the test (0.09% vs 0.8%).

## Conclusion?

Frankly, I don't know. One thing is for sure; one can use statistics to steer an "average person" towards the desired decision. If my goal is to increase reduce the number of women who undergo routine mammogram tests, I will talk in terms of absolute risk (9%). If, on the other hand, I'm selling mammogram equipment, I will definitely talk in terms of the odds ratio, i.e., the 100-times risk increase. Think about this every time someone is talking to you about hazards.
