---
layout: post
title: "Sometimes, you don't really need a legend"
date: 2019-10-28
categories: 
  - "blog"
  - "data-visualization"
tags: 
  - "because-you-can"
  - "data-visualisation"
  - "data-visualizatin"
  - "dataviz"
  - "legend"
coverImage: "/assets/images/2019/10/photoz.jpeg"
---

This is another "[because you can](https://gorelik.net/tag/because-you-can/)" rant, where I claim that the fact that you can do something doesn't mean that you necessarily need to.

This time, I will claim that sometimes, you don't really need a legend in your graph. Let's take a look at an example. We will plot the GDP per capita for three countries: Israel, France, and Italy. Plotting three lines isn't a tricky task. Here's how we do this in Python

```
plt.plot(gdp.Year, gdp.Israel, '-', label='Israel')
plt.plot(gdp.Year, gdp.France, '-', label='France')
plt.plot(gdp.Year, gdp.Italy, '-', label='Italy')
plt.legend()
```

The last line in the code above does a small magic and adds a nice legend

![This image has an empty alt attribute; its file name is image.png](/assets/images/2019/10/image.png?w=388)

In Excel, we don't even need to do anything, the legend is added for us automatically.

![This image has an empty alt attribute; its file name is image-1.png](/assets/images/2019/10/image-1.png?w=1024)

### So, what is the problem?

What happens when a person wants to know which line represents which country? That person needs to compare the line color to the colors in the legend. Since our working memory has a limited capacity, we do one of the following. We either jump from the graph to the legends dozens of times, or we try to find a heuristic (a shortcut). Human brains don't like working hard and always search for shortcuts (I recommend reading Daniel Kahneman's "Think Fast and Slow" to learn more about how our brain works).

What would be the shortcut here? Well, note how the line for Israel lies mostly below the line for Italy which lies mostly below the line for France. The lines in the legend also lie one below the other. However, the line order in these two pieces of information isn't conserved. This results in a cognitive mess; the viewer needs to work hard to decipher the graph and misses the point that you want to convey.

And if we have more lines in the graph, the situation is even worse.

![This image has an empty alt attribute; its file name is image-2.png](/assets/images/2019/10/image-2.png?w=388)

### Can we improve the graph?

Yes we can. The simplest way to improve the graph is to keep the right order. In Python, we do that by reordering the plotting commands.

```
plt.plot(gdp.Year, gdp.Australia, '-', label='Australia')
plt.plot(gdp.Year, gdp.Belgium, '-', label='Belgium')
plt.plot(gdp.Year, gdp.France, '-', label='France')
plt.plot(gdp.Year, gdp.Italy, '-', label='Italy')
plt.plot(gdp.Year, gdp.Israel, '-', label='Israel')
plt.legend()
```

![This image has an empty alt attribute; its file name is image-3.png](/assets/images/2019/10/image-3.png?w=388)

We still have to work hard but at least we can trust our brain's shortcut.

### If we have more time

If we have some more time, we may get rid of the (classical) legend altogether.

```
countries = [c for c in gdp.columns if c != 'Year']
fig, ax = plt.subplots()
for i, c in enumerate(countries):
    ax.plot(gdp.Year, gdp[c], '-', color=f'C{i}')
    x = gdp.Year.max()
    y = gdp[c].iloc[-1]
    ax.text(x, y, c, color=f'C{i}', va='center')
seaborn.despine(ax=ax)
```

(if you don't understand the Python in this code, I feel your pain but I won't explain it here)

![This image has an empty alt attribute; its file name is image-4.png](/assets/images/2019/10/image-4.png?w=417)

Isn't it better? Now, the viewer doesn't need to zap from the lines to the legend; we show them all the information at the same place. And since we already invested three minutes in making the graph prettier, why not add one more minute and make it even more awesome.

![This image has an empty alt attribute; its file name is image-5.png](/assets/images/2019/10/image-5.png?w=521)

This graph is much easier to digest, compared to the first one and it also provides more useful information.

.

![This image has an empty alt attribute; its file name is image-6.png](/assets/images/2019/10/image-6.png?w=521)

I agree that this is a mess. The life is tough. But if you have time, you can fix this mess too. I don't, so I won't bother, but Randy Olson had time. Look what [he did in a similar situation](http://www.randalolson.com/2014/06/28/how-to-make-beautiful-data-visualizations-in-python-with-matplotlib/).

![percent-bachelors-degrees-women-usa](/../assets/images/2019/10/percent-bachelors-degrees-women-usa.png)

I also recommend reading my older post where I [compared graph legends to muttonchops](https://gorelik.net/2017/04/12/chart-legends-and-the-muttonchops/).

### In conclusion

Sometimes, no legend is better than legend.

This post, in Hebrew: \[[link](https://he.gorelik.net/?p=74)\]
