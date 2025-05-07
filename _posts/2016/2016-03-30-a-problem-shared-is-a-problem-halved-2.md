---
title: "A problem shared is a problem halved"
date: 2016-03-30
categories: 
 - "blog"
tags: 
 - "blogging"
 - "persistence"
 - "sna"
 - "social"
 - "social-network-analysis"
 - "survival"
cover_image: "/assets/img/2016/03/a-problem-shared-is-a-problem-halved.png"
layout: "post"
---

## Social factors that promote persistent blogging

<span style="line-height:1.5;"><img class="alignright" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Ilia_Efimovich_Repin_%281844-1930%29_-_Volga_Boatmen_%281870-1873%29.jpg/1200px-Ilia_Efimovich_Repin_%281844-1930%29_-_Volga_Boatmen_%281870-1873%29.jpg" alt="" width="400" height="185"><span style="color:#993300;"><em>Socially active bloggers, and bloggers who write in teams tend to write a blog for longer times.</em></span></span>

<span style="line-height:1.5;">Writing a blog is a hard and demanding task. It requires creativity, dedication and persistence. Data shows that a large percentage of bloggers stop posting after a couple of months, and most of them don’t survive for more than a year. What is the force that drives the successful bloggers? What factors distinguish the persistent bloggers from the “quitters”? Is there anything a person can do to increase his or her chances to keep blogging and not to quit?</span>

 

### Competing theories

The research that I will present here was performed in collaboration with Lior Zalmanson, a post-doc researcher at Stern School of Business New York University. In this study, we asked ourselves whether people can increase their chance to keep blogging by joining forces.

Whether people work better in groups or as individuals is an open and long-debated question in social psychology. On one hand, there is a phenomenon of “Social Loafing” - a phenomenon that was first described by a French agricultural engineer Maximilien Ringelmann in  According to Ringelmann’s findings, having group members work together on a task results in significantly less effort than when individual members are acting alone [[Wikipedia](https://en.wikipedia.org/wiki/Ringelmann_effect), [Original paper](http://gallica.bnf.fr/ark:/12148/bpt6k54409695.image.f14.langEN)].

On the other hand, Otto Köhler, a German psychologist, has found in 1926 that the weaker group members strive to keep up with the accomplishment of the other group members, which results in an overall performance improvement [[Enc Britanica](http://www.britannica.com/topic/Kohler-effect)]. The effect of “Social Compensation” was suggested by [Karau and Williams in 1991](http://www.communicationcache.com/uploads/1/0/8/8/10887248/social_loafing_and_social_compensation-_the_effects_of_expectations_of_co-worker_performance.pdf). According to their observations, a worker will work harder in groups, compensating for those who work less.

### The connected world of WordPress.com bloggers

Which of the two competing theories is more applicable towards the world of bloggers? To shed some light on this question, we studied the blogging patterns of WordPress.com users. WordPress.com is a platform that hosts more than 110,000,000 sites that belong to more than 102,000,000 registered users. To better understand the implications of social interactions on blogging activities, we analyze the links between WP.com users and blogs.
This analysis results in a mathematical structure called ‘graph’ that contains different types of interactions among various kinds of entities.

![halved_01](/assets/img/2016/03/halved_01.png){:width="730" :class="alignnone"}

Let’s consider a simple example. Alice who wrote a post on her blog. The fact of publishing a post created a relationship between Alice and her blog. We will call this connection “IS_CONTRIBUTOR”. At some point, Bob joins Alice and writes a post to the same blog. Now, both Alice and Bob are contributors of that blog.

As time passes by, Bob continues submitting content to the blog and Alice doesn’t. To reflect this difference between the two, we define a “weight” of a link — the more content a user contributes to the blog, the higher is the weight. If a user, Alice in our case, doesn’t write new content to the blog her connection to the blog gradually disappears until at some time we will delete the link. We will no longer consider Alice as a contributor to B1.

At some point, Charlie reads Alice’s blog post and presses the “like” button. By clicking this button, a connection between Charlie and Alice is created. We will call this relationship “LIKES_AUTHOR”. We consider bringing a new audience to a blog as a contribution to that blog. Thus, when Charlie “likes” Alice’s post, he also increases the “IS_CONTRIBUTION” link between Alice and the blog.

![halved_02](/assets/img/2016/03/halved_02.png){:width="730" :class="alignnone"}

For the sake of our discussion, let’s assume that Alice writes posts in another blog, we will call it B It turns out that Daphne and Eve are also authors in B Charlie, whom we already met, is also writing a blog, all by himself.

![halved_03](/assets/img/2016/03/halved_03.png){:width="730" :class="alignnone"}

We want to know how collaboration affects authors’ persistence. In other words: does the number of collaborators an author has have an impact on the probability that that author will keep blogging for a longer time. In this toy example, Alice has three collaborators (Bob, Daphne and Eve), Daphne and Eve have both two collaborators; Bob has only one collaborator (Alice), and Charlie has no collaborators at all. In order not to upset writers who write alone, we will consider a person a partner of him or her selves. Thus, for the purpose of our analysis, Alice has four collaborators (including herself), Daphne and Eve have three, and Bob has two collaborators.

<table>
<thead>
<tr>
  <th>Author</th>
  <th># of collaborators</th>
</tr>
</thead>
<tbody>
<tr>
  <td>Alice</td>
  <td>4</td>
</tr>
<tr>
  <td>Bob</td>
  <td>2</td>
</tr>
<tr>
  <td>Charlie</td>
  <td>1</td>
</tr>
<tr>
  <td>Daphne</td>
  <td>3</td>
</tr>
<tr>
  <td>Eve</td>
  <td>3</td>
</tr>
</tbody>
</table>

What we see here is a small example. In reality, WordPress.com users form a large complex network of people and blogs. Since the connections between the nodes in this network can appear and disappear, this network is in constant change. One of the interesting things that we can do with this kind of dynamic systems is to discover user communities. I have already presented one such an analysis in the past (see [this presentation](https://www.youtube.com/watch?v=5OfLTddasAA)) and will certainly show more of it in the future. Meanwhile, note that blogs don’t exist in a vacuum. Most of the time, people who write don’t write for themselves, they seek an audience. Writing inside a large platform of many interconnected communities brings the author closer to such an audience and promotes discussion and exchange of ideas.

![halved_04](/assets/img/2016/03/halved_04.png){:width="730" :class="alignnone"}

### Collecting the data

There are many types of communities in the online world. There are also many types of collaboration between people. Let us now concentrate on a very specific kind of community — a community of writers. In this analysis, we treat a blog or a website as a gathering point and all the writers in that website as the community members. We can tackle the question raised at the beginning of this post: what makes some bloggers keep blogging?
To answer this question, we look at people who opened a WordPress.com account during the thirteen months from Jan 2013 and Feb  WordPress.com is a home of large professional (VIP) customers such as NBC Sports, TED, CNN, Time and others (https://vip.wordpress.com/clients/). It would be unfair to include these professional writers in our analysis. Unfortunately, some people use WordPress.com for spamming, fraud and other non-legit activities; we have removed those people from the analysis. Many people open a WordPress.com account, write a test post and go away. We did not like to include such users in this study, so we only included those people who gave or received, at least, one “like”, as a substitute for a minimal level of quality and commitment. Last but not least, we excluded the 400+ Automattic employees and contractors from the analysis. In Automattic, we use WordPress.com for internal communication purposes and are a clear outlier in any analysis.

When we look at monthly snapshots of the dynamic networks mentioned above, we collect various descriptive statistics about the users who registered two to three months before the snapshot. We believe that this period is long enough for novice users to accommodate with the platform and to gain some popularity and social ties. Next, we look at the monthly snapshot made one year later and check whether a current user appears in the network as a contributor to at least one blog or not. We consider the users who appear in this graph as survivors. For the purpose of this analysis, we completely ignore what happens during the entire year — between the two snapshots.

![halved_05](/assets/img/2016/03/halved_05.png){:width="730" :class="alignnone"}

In the end, we need to analyze the connection between two sets of information. On one hand we have the descriptive statistics collected at the data collection point. On the other side of the equation, we have the survival information. Let’s see the results.

### Silver bullet of blogging success?

Approximately 570,000 authors met the study inclusion criteria. We don’t analyze these authors alone but in a context of a network that contains about 5,000,000 users. What factors promote author survival? In the next paragraphs, I will show several similar graphs. In these graphs, the Y-axis will show the probability to continue blogging, as a function of the variable presented on the X-axis. On that axis, below the number that represents variable value, you will find the number of people for whom this true.

[caption id="attachment_92" align="alignnone" width="650"]![The more incoming likes authors receive, the higher is their survival probability](/assets/img/2016/03/halved_06.png){:width="650"} The more incoming likes authors receive, the higher is their survival probability[/caption]

The figure above shows how the survival probability depends on the number of likes an author received two to three months after the registration. We can see that there were 172 thousand users who did not get any “like” at the data collection point. These authors had a 2% probability to stay active at the end of the study. Approximately 213 thousand users with one “like” had the probability to keep blogging of 4% — a two-fold increase. Overall, we see that the more “likes” a person receives, the higher is the survival probability. Users who received more than 32 likes (there were only 800 of them) are 43% likely to keep blogging (the shaded area represents the 95% confidence interval — how confident we are in the survival estimate).

Can this graph help an aspiring blogger? Not directly. It doesn’t surprise that an author who is capable of producing high-quality content that is also popular with a broad audience will also be likely to continue blogging in the future. Plus, authors can’t directly affect the number of likes they receive. Unlike receiving likes, pressing the “like” button on other’s content is under a person’s direct control. The following graph shows survival probability as a function of how many “likes” a user gave to others.

[caption id="attachment_93" align="alignnone" width="650"]![The more likes authors give, the higher is their probability to survive](/assets/img/2016/03/halved_07.png){:width="650"} The more likes authors give, the higher is their probability to survive[/caption]

Generally speaking, the more socially active the authors are, the more likely they are to keep blogging. It is interesting to note that there is such a thing as too much love: authors who pressed the “like” button more than 32 times during their first two to three months are less likely to survive, compared to the immediately preceding group.
At first glance, one might take the two graphs above as a magic recipe for blogging success. Doing this will be a mistake. It is correct that we have found a correlation between the number of incoming and outgoing likes and the survival probability. This connection does not tell us which of the two sides of the association is the cause and which one is the result. This uncertainty, which is often called the correlation-causation question, is very hard to solve. However, based on my general knowledge of human psychology, I claim that social interactions are partially responsible for the high correlation that we see in the data.

### A problem shared is a problem halved

Let’s get back to our original question: do authors who collaborate with others have a higher probability to keep on blogging? In the terms of our example network, does Alice, who has four collaborators, have greater chance to survive, compared to Charlie, who writes by himself? The answer is yes. According to the data we have, authors who write by themselves have only a 6% probability to keep blogging till the end of the study. Authors who write in pairs have a 9% probability to stay — a 50% increase. Interestingly, subsequent addition of collaborators has almost no effect, until we see teams of more than 16 authors.

[caption id="attachment_94" align="alignnone" width="648"]![Authors who write in groups are more likely to continue writing](/assets/img/2016/03/halved_08.png){:width="648"} Authors who write in groups are more likely to continue writing[/caption]

### Does fairness matter?

This discussion started with a description of two competing theories that try to predict the outcome of a joined effort. Both theories talk about “weaker” and “stronger” participants. It turns out that we can measure the extent to which a person contributes to a blog and the extent to which blog’s authors provide equal contributions. Let’s get back to our example network. Suppose that, at some point we notice that Alice, Bob and Charlie collaborated in submitting content to a blog (B1). Alice wrote most of the posts and attracted most of the “likes”; Bob wrote from time to time; and Charlie contributed only one post, long time ago. If we measure link strength between each author and this particular blog, we see that Alice’s contribution is 10, Bob’s contribution is 0.5 and Charlie’s contribution is 0. On the other hand, Charlie and Daphne and Eve occasionally write a joined blog (B2) to which they contribute equally, with tie strength values of 0.1 each.

![halved_09](/assets/img/2016/03/halved_09.png){:width="730" :class="alignnone"}

Will Alice feel abused by Charlie and Bob and cease her collaboration with them? Is it possible that Charlie will feel insecure about his weak cooperation with Alice and Bob, and will only write to B2? We can record how unbalanced a user’s input is in a given blog. We will measure this type of inequality such that authors who contribute less than the average will receive negative values; authors who provide the average contribution will have inequality value of zero and authors who perform most of the job will have a positive inequality score. We compute this score for each person-blog connection, which means that people who contribute to several blogs will have several inequality scores.

<table>
<thead>
<tr>
  <th>Blog</th>
  <th>Author</th>
  <th>Contribution</th>
  <th>Inequality score</th>
</tr>
</thead>
<tbody>
<tr>
  <td>B1</td>
  <td>Alice</td>
  <td>10</td>
  <td>1</td>
</tr>
<tr>
  <td></td>
  <td>Bob</td>
  <td>5</td>
  <td>0</td>
</tr>
<tr>
  <td></td>
  <td>Charlie</td>
  <td>0.1</td>
  <td>-6</td>
</tr>
<tr>
  <td>B2</td>
  <td>Charlie</td>
  <td>0.1</td>
  <td>0</td>
</tr>
<tr>
  <td></td>
  <td>Daphne</td>
  <td>0.1</td>
  <td>0</td>
</tr>
<tr>
  <td></td>
  <td>Eve</td>
  <td>0.1</td>
  <td>0</td>
</tr>
</tbody>
</table>

What is the probability of a given author to continue contributing to a particular blog, given how equal (or unequal) person’s contribution to this blog is. Note, that a user who contributes to several blogs may stop writing to one blog, but continue adding content to another one. In our latest example, Charlie may decide that he doesn’t want to write to B1 anymore and will contribute only to B2.
Generally speaking, there may be four types of connection between the inequality score and the persistence probability as schematically depicted in the figure below:

![halved_10](/assets/img/2016/03/halved_10.png){:width="730" :class="alignnone"}

One possible outcome is that the more a person contributes to a blog, the higher is the chance that he or she will continue writing to that blog (case A in the figure above). Another possibility is that the opposite is the truth: the more a person contributes to the blog, the smaller is the chance to keep writing (for example, due to the sense of unfairness; case B). Another possibility is that the average contributing people will have a higher chance to drop off, leaving only the super engaged and occasional contributors (case C). Finally, an opposite possibility exists, where average-contributing authors have the highest chance to persist.

According to our data, option A seems to describe better the reality. Contrarily to my initial belief, people don’t mind carrying the load. To some extent, authors who contribute more than the average to the joined effort are more likely to keep writing.

[caption id="attachment_97" align="alignnone" width="689"]![halved_11](/assets/img/2016/03/halved_11.png){:width="689"} Authors who contribute more are more likely to survive[/caption]

There is another level to analyze contribution inequality. If you go back to our latest example, you’ll notice that the contributions to B1 are very balanced, while the contributions to B1 are not. To quantify such a balance we use the Gini index. The Gini index is in extensive use in economics. It was developed to measure the extent to which the distribution of a limited resource among individuals deviates from a perfectly equal distribution. The Gini index ranges from zero to one. The value of zero means total equality, and one means the strongest inequality possible. Taken in the example above, blog B1 has the Gini index of 0.44 and B2 has the index of 0.
Having computed the Gini index for all the blogs in our study, we can analyze the connection between the Gini index and the probability of a blog to survive one year after the analysis. Similarly to the previous case, there are four possible relationships between the measured value (Gini index) and the probability:

![halved_12](/assets/img/2016/03/halved_12.png){:width="730" :class="alignnone"}

I must admit that before the analysis, I expected to see a curve similar to the case B. I was very surprised (and super excited) to see that sites with extreme input inequality have much higher survival probability, compared to the overall equal blogs.

[caption id="attachment_99" align="alignnone" width="603"]![Blogs with highly dominant contributors are more likely to survive](/assets/img/2016/03/halved_13.png){:width="603"} Blogs with highly dominant contributors are more likely to survive[/caption]

### Conclusions

Let me go back to the questions I asked at the beginning of this post.

**Q: What is the force that drives the successful bloggers? **

**Q: What factors distinguish the persistent bloggers from the “quitters”? **

I have shown an empirical evidence that social interaction with other authors is strongly correlated to blogging success. Does social interaction bring blogging success, or are highly motivated authors also active in inter-personal activity? I don’t know for sure, but I assume that the reality is a combination of both. Thus, when choosing a blogging platform, make sure you can interact with your readers and with bloggers with similar interests. Make sure to connect with them. You can only gain from these connections.

**Q: Is there anything a person can do to increase his or her chances to keep blogging and not to quit? **

Team up! The evidence is clear: people who write in groups are more likely to keep writing. Every project needs a leader (recall the inequality graphs). If you are already motivated, don’t be afraid to lead. On the other hand, don’t be scared to be in the shadow of a dominant partner. Unbalanced contribution to a joint project is not about unfairness but is about leadership. Remember that 1% of fame is better than 100% of anonymity.

The information in this post was first presented at [WordCamp Israel](https://2016.israel.wordcamp.org/) that took place in Jerusalem on March 28,  This study was performed in tight collaboration with Lior Zalmanson, a post-doc researcher in the Stern School of Business, New York University.

[![Opening slide](/assets/img/2016/03/screen-shot-2016-03-30-at-10-01-42.png){:width="262" :class="alignnone"}](https://2016.israel.wordcamp.org/)
