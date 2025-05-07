---
title: "What is the best way to handle command line arguments in Python?"
date: 2018-02-10
categories: 
 - "blog"
tags: 
 - "cli"
 - "python"
layout: "post"
---

The best way to handle command line arguments with Python is `[defopt](http://evanunderscore/defopt: Effortless argument parser)`. It works like magic. You write a function, add a proper docstring using any standard format (I use [[numpy doc](https://github.com/numpy/numpy/blob/master/doc/HOWTO_DOCUMENT.rst.txt)]), and see the magic

[code language="python"]

import defopt

def main(greeting, *, count=1):
    """Display a friendly greeting.

    :param str greeting: Greeting to display
    :param int count: Number of times to display the greeting
    """
    for _ in range(count):
        print(greeting)

if __name__ == '__main__':
    defopt.run(main)
[/code]

 

You have:


     help string generation

     data type conversion

     default arguments

     zero boilerplate code

Magic!

![Illustration: the famous XKCD ](/assets/img/2018/02/python.png){:width="264" :class="aligncenter"}
