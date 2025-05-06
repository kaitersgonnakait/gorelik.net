---
layout: post
title: "The difference between python decorators and inheritance that cost me three hours of hair-pulling"
date: 2020-02-03
categories: 
  - "blog"
tags: 
  - "decorators"
  - "frustration"
  - "inheritance"
  - "python"
---

I don't have much hair on my head, but recently, I encountered a funny peculiarity in Python due to which I have been pulling my hair for a couple of hours. In retrospect, this feature makes a lot of sense. In retrospect.

First, let's start with the mental model that I had in my head: inheritance.

Let's say you have a base class that defines a function \`f\`

![](/assets/images/2020/02/image.png?w=656)

Now, you inherit from that class and rewrite `f`

![](/assets/images/2020/02/image-1.png?w=684)

What happens? The fact that you defined `f` in `ClassB` means that, to a rough approximation, the old definition of `f` from `ClassA` does not exist in all the `ClassB` objects.

Now, let's go to decorators.

```python
@dataclass_json
@dataclass
class Message2:
    message: str
    weight: int
    def to_dict(self, encode_json=False):
        print('Custom to_dict')
        ret = {'MESSAGE': self.message, 'WEIGHT': self.weight}
        return ret
m2 = Message2('m2', 2)
```

What happened here? I used a decorator \`dataclass\_json\` that, among other things, provides a \`to\_dict\` function to Python's [data classes](https://docs.python.org/3/library/dataclasses.html). I created a class \`Message2\`, but I needed s custom \`to\_dict\` definition. So, naturally, I defined a new version of \`to\_dict\` only to discover several hours later that the new \`to\_dict\` doesn't exist.

Do you get the point already? In inheritence, the custom implementations are added ON TOP of the base class. However, when you apply a decorator to a class, your class's custom code is BELOW the one provided by the decorator. Therefore, you don't override the decorating code but rather "underride" it (i.e., give it something it can replace).

As I said, it makes perfect sense, but still, I missed it. [I don't know whether I would have managed to find the solution without Stackoverflow](https://stackoverflow.com/questions/59882545/why-cant-i-override-to-dict-method-of-a-dataclass-object-that-uses-datacla/59884043#59884043).
