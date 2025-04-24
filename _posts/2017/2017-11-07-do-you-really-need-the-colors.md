---
layout: post
title: "Do you REALLY need the colors?"
date: 2017-11-07
categories: 
  - "blog"
tags: 
  - "bar-plot"
  - "because-you-can"
  - "before-after"
  - "colors"
  - "data-visualization"
  - "dataviz"
coverImage: "/assets/images/2017/11/one-vs-another.png"
---

[Seaborn](https://seaborn.pydata.org) is a Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics. Look at this example from the seaborn [documentation site](https://seaborn.pydata.org/generated/seaborn.barplot.html)

```
>>> import seaborn as sns
>>> sns.set_style("whitegrid")
>>> tips = sns.load_dataset("tips")
>>> ax = sns.barplot(x="day", y="total_bill", data=tips)
```

![Barplot example with colored bars](/assets/images/2017/11/barplot_before.png)

This example shows the default barplot and is the first barplot. Can you see how easy it is to add colors to the different columns? But WHY? What do those colors represent? It looks like the only information that is encoded by the color is the bar category. We already have this information in the form of bar location. Having this colorful image adds nothing but a distraction. It is sad that this is the default behavior that seaborn developers decided to adopt.

Look at the same example, without the colors

```
>>> ax = sns.barplot(x="day", y="total_bill", color='gray', data=tips)
```

![Barplot example with gray bars](/assets/images/2017/11/barplot_after.png)

Isn't it much better? The sad thing is that a better version requires memorizing additional arguments and more typing.

This was my [because you can](https://gorelik.net/tag/because-you-can/) rant.
