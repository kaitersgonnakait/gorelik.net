---
layout: post
title: "Can error correction cause more error? (The answer is yes)"
date: 2018-10-09
categories: 
  - "blog"
tags: 
  - "distribution"
  - "statistics"
---

This is an interesting thought experiment. Suppose that you have some appliance that acts in a normally distributed way. For example, a [nerf gun](https://www.youtube.com/watch?v=uJgzam4c-0Y). Let's say now that you aim and fire the gun. What happens if you miss by some amount of X? Should you correct your aim in the opposite direction? My intuition says "yes." So does the intuition of many other people with whom I talked about this problem. However, when we start thinking about this problem, we realize that the intuition is wrong. Since we aim the gun, our assumption should be that the deviation is zero. A single observation is not sufficient to reject this assumption. By continually adjusting the data generating process based on a single observation, we reduce the precision (increase the dispersion). Below is a simulation of adjusted and non-adjusted processes (the code is [here](https://gist.github.com/bgbg/be27992f5370e79e96d31c00a5f18adf)). The broader spread of the adjusted data (blue line) is evident.

![Two curves. Blues: high dispersion of values when adjustments are performed after every observation. Orange: smaller dispersion when no adjustments are done.](/assets/images/2018/10/adjustments1.png)

Due to the nature of the normal random variable, a single large accidental deviation can cause an extreme "correction," which in turn will create a prolonged period of highly inaccurate points. This is precisely what you see in my simulation. The moral of this simple experiment is that you shouldn't let a single affect your actions.
