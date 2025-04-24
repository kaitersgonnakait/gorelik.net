---
layout: post
title: "Gender salary gap in the Israeli high-tech"
date: 2018-02-01
categories: 
  - "blog"
tags: 
  - "data-visualization"
  - "gender"
  - "gender-inequality"
  - "israel"
  - "salary"
  - "work"
coverImage: "/assets/images/2018/02/figure_003_two_periods_.png"
---

A large and popular Israeli Facebook group, "[The High-Tech Troubles](https://www.facebook.com/groups/hitechproblems/)," has recently surveyed its participants. The responders provided personal, demographic, and professional information. The group owners have published the aggregated results of that survey. In this post, I analyze a particular aspect of these findings, namely, how the responders' gender and experience affect their salary. It is worth noting that this survey is by no means a representative one. It's most noticeable but not the only problem is the participation bias. Another problem is the fact that the result tables do not contain any information about the number of responders in any group. Without this information, it is impossible to compute confidence intervals of any findings. Despite these problems, the results are interesting and worth noting.

The data that I used in my analysis is available in [this spreadsheet](https://docs.google.com/spreadsheets/d/1YOKIYLrC4kHXW-2DoMuUnH8Q_gWf-m89jpDwXh_IdjA/htmlview?usp=sharing&sle=true). The survey organizers promise that they excluded groups and categories with insufficiently few answers, and we have to trust them in that. The results are divided into twenty professional categories such as 'Account Management,' 'Data Science', 'Support' and 'CXO' (which stands for an executive role). The salary groups are organized in exponential bins according to the years of experience: 0-1, 1-2, 2-4, 4-7; and more than seven years of experience. Some of the cell values are missing, I assume that these are the categories with too few responders. I took a look at the gap between the salary reported by women and the compensation reported by men.

Let's take a look at the most complete set of data -- the groups of people with 1-2 years of experience. As we may see from the figure below, in thirteen out of twenty groups (65%), women get less money than men. ![Gender compensation gap, 1-2 years of experience. Women earn less in 13 of 20 categories](/assets/images/2018/02/figure_001_one_year_.png)

Among the workers with 1 - 2 years of experience, the most discriminating fields are executives and security researchers. It is interesting to note the difference between two closely related fields: Data Science and BI/Data Analysts. The former is considered a more lucrative position. On average, the male data scientists get 11% more than their female colleagues, while male data analysts get 13% less than their female counterparts. I wonder how this difference relates to my (very limited) observation that most of the people who call themselves a BI expert are females, while most of the data scientists whom I know are males.

As we have seen, there is no much gender equality for the young professionals. What happens when people gain experience? How does the gender compensation gap change after eight years of professional life? The situation is even worse. In fourteen, out of sixteen available fields, women get less money than men. The only field in which it pays to be a woman is the executive roles, where the women get 19% more than the men.

![Gender compensation gap, more than 7 years of experience. Women earn less in 14 of 16 categories](/assets/images/2018/02/figure_002_seven_years_.png)

To complete the picture, let's look at the gap dynamics over the years in all the occupation fields in that report.

![Gender gap dynamics. 20 professional fields over different experience bins](/assets/images/2018/02/figure_004_dynamics_.png)

### What do we learn from these findings?

These findings are real. We cannot use the non-representativity of these data, and the lack of confidence intervals to dismiss these findings. I don't expect the participants to lies, neither do I not expect any bias from the participation patterns. It is true that I can't obtain confidence intervals for these results. However, the fact that the vast majority of the groups lie on one side of the equality line suggests the overall validity of the gender gap notion. How can we fix this gap? I frankly don't know. As a father of three daughters (9, 12, and 14 years old), I talk to them about this gap. I make sure they are aware of this problem so that, when it's their turn to negotiate compensation, they are aware of the systematic bias. I hope that this knowledge will give them the right tools to fight for justice.
