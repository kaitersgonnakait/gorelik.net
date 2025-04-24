---
layout: post
title: "Single-handedly Development: A Recipe for Troubles"
date: 2023-09-04
categories: 
  - "blog"
  - "career-advice"
  - "direction-matters"
---

\[[copied from my Substack newsletter](https://directionmatters.substack.com/p/single-handedly-development-a-recipe)\]

The subject of this post primarily revolves around creators of digital solutions, such as programmers, designers, analysts, and data scientists. Regardless of whether you identify as one or manage one, I assure you there's a valuable takeaway for all within this read.

We often encounter "lone wolves," individuals who are the sole professional in their field within their organization. This situation typically arises when the company lacks the resources to employ more than one programmer, designer, or analyst. Such circumstances can pose significant risks and necessitate proper risk management. 

Now, you may say, "What about C-level managers? They too are often the sole professionals in their field, and working alone is the norm." I'll try to address the scenario of C-levels later, but let's concentrate on everyone else.

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1165fd9b-914b-4efc-9a44-2024ff4a2a79_1538x620.png)

## What's the big deal?

So, what's the big deal?

To put it succinctly, we're discussing knowledge workers: individuals who translate their brain prowess into value. To maximize this value creation, the process needs to be as efficient and honed as possible. The Talmud tells us about rabbi Hama bar Hanina who said, "Just as a knife is sharpened only by the steel of its mate, so too, a scholar \[ knowledge worker, in our context\] is sharpened only by his fellow." When knowledge workers lose that sharpness, the quality of their work suffers. The output becomes suboptimal due to a lack of adversarial oversight, the curse of knowledge, and the bus factor. Let's delve into each of these aspects.

### Lack of adversarial oversight

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e69e5ac-e887-426f-a229-d1abb4e12f6e_1064x134.png)

When I operate within a team alongside peers, I understand that my work is continually subject to review. This can, and should, be a formal review process, such as code review in programming. But it can also take the form of informal exchanges of ideas during daily communication. A healthy organization fosters a culture of review and constructive debates. In such an environment, everyone is expected to receive and offer feedback, everyone anticipates being challenged and to challenge others. This potential for critique and the ongoing drive to critique others maintain a state of alertness and motivation for continuous improvement. 

The Talmud, which I mentioned earlier, is full of records of scholars disputing and challenging one another. That's how these scholars ensured their constant intellectual growth. The renowned philosopher Karl Popper presented the concept of risky predictions, suggesting that any hypothesis—or piece of code, for that matter—should be bold enough to potentially be proven incorrect. If these bold assertions undergo testing and remain unrefuted, they are deemed accurate and, I would add, their author is deemed credible.

Now, consider our Lone Wolf. There's no one to criticize them, no one to review their work, and no one requiring their review for their own tasks. The Lone Wolf's colleagues hold deep respect for them because they're the only ones in the team who know how to program, design a logo, or perform p-hacking. They admire the Lone Wolf, they appreciate the Lone Wolf, but they fail to sharpen the Lone Wolf's skills.

### The curse of knowledge

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0acea08c-e006-4aa3-9f8e-c4291348dde3_1818x338.png)

Rarely do you know what I don't know. What may seem trivial to you could be completely enigmatic to me, and you might not even realize it. This phenomenon is known as the "curse of knowledge."

One issue associated with the curse of knowledge relates to the first point of this post, the absence of oversight. When certain pieces of information seem obvious, you start treating your hypotheses and assumptions as facts and behave accordingly. Another risk is that the curse of knowledge can lead to inadequate planning and documentation.

When working solo on a small or moderately-sized project, you know exactly what's happening within it. To onlookers, you resemble the archetypal chef in the kitchen, effortlessly grabbing the sharpest knife from the drawer without a second glance and instinctively knowing where every spice jar is located. 

But this seamless workflow can falter when one of two scenarios occurs: either your project becomes too large for you to manage all its details mentally, or a new member joins your team. In both cases, you start losing time trying to remember which function performs the preprocessing, which directory houses the client's mockups, and which file contains the up-to-date data versus which one is merely a backup. Consequently, your code becomes less clean, you design against incorrect mockups, and your analysis is flawed. Worse still, you produce these substandard results in quadruple the time it would have taken had you properly planned and documented.

The risk of such chaos is significantly reduced when two or more colleagues collaborate in a team. Like dance partners, they must be careful not to step on each other's toes, which encourages them to dedicate time to planning and documentation. As a team, they have more strength to resist the constant pressure to sacrifice quality, planning, and documentation for speed.

### The bus factor

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0d86bda-12a5-422c-8368-8a6528e5ac3a_1850x674.png)

The bus factor refers to the risk associated with information and capabilities not being shared among team members, a concept that draws from the hypothetical scenario of 'what if they were hit by a bus.' Of course, we don't need to be so morbid. Team members can leave their roles for various reasons: they might become parents, win the lottery, choose a monastic life, or any other myriad of joyful reasons. When a team member departs, there should exist some level of redundancy to compensate for the expertise lost. The issue with a lone professional leaving the organization extends beyond having no one to perform their tasks; there's also no one who \*\*knows\*\* how to perform their tasks.

Onboarding a replacement for a team member is always a challenge. However, since the Lone Wolf wasn't subjected to constant reviews (lack of oversight) and didn't allocate enough time for planning and documentation (remember the curse of knowledge?), what is a challenge for a multi-member team escalates into a nightmare that can halt operations for weeks or even months. I personally witnessed first-hand situations like this. I personally saw thousands of lines of code rewritten from scratch because nobody knew how it worked.  

This resulting chaos not only disrupts workflow but also creates undue stress on the remaining team members and the new recruit, who must scramble to fill a knowledge gap without a clear roadmap. It's a stark reminder of the importance of collaborative processes and shared understanding within a team.

## Is there a solution?

[![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4085bc2b-83e7-4f34-b3af-253226cc0fad_950x320.png)

The old saying goes, "It's better to be young, healthy, and wealthy than old, sick, and poor." Similarly, it's obviously preferable to hire at least two professionals for each role. However, this isn't always feasible. Even if budget isn't a constraint, you might not require two designers, analysts, or programmers on your team. Having a bored knowledge worker is an issue in itself, warranting a separate discussion. 

So, what alternatives are there? One approach to mitigating this issue is to introduce a part-time colleague, a co-pilot, or a proverbial sidekick—either as a hired employee or a freelancer. This additional team member's role would be to serve as a sharpening tool for your Lone Wolf, their sparring partner, someone with whom they can exchange ideas, ensure nothing is taken for granted, and verify that the correct processes are adhered to. For this arrangement to be effective, the co-pilot should not be a one-time visitor but rather a regular contributor. They need to understand your company's business and culture and become a part of its institutional memory. In this way, you not only ensure a proper workflow but also safeguard against embarrassing bugs and unforeseen departures. 

One of the services I provide aligns exactly with this solution, and you're encouraged to reach out if you're seeking a collaborator for your Lone Wolf.
