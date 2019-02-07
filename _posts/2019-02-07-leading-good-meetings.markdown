---
layout: post
title: The Key to Leading Great Meetings as a Data Scientist? Empathy.
date: 2019-02-07 11:32:20 +0300
description: how-to on leading great meetings, geared toward technical folks
img: chaos.jpg
tags: [technical leadership, productivity]
---
During my first year working as a Data Scientist, I bombed a presentation in front of my company's C-Suite team.

I walked out of the meeting feeling crushed, and like I had just wasted everyone's time. But I was also surprised.
In my prior life as a management consultant I was lucky enough to work alongside and learn from some skilled managers
who had mastered the art of communicating complex material. Given the degree of practice I had from consulting,
it surprised me that this most recent presentation had gone so poorly. But what if I hadn't applied the same process to
this presentation? As it turns out, that I hadn't.

>Leading up that presentation, I spent 95% of my time on the technical stuff: loading data,
cleaning data, modeling data, testing, and generating results. I spent the remaining 5% hastily pasting
the outputs of my model into a slide deck. No wonder things had gone wrong!

I've observed that in industry, communicating our results often takes a backseat. Sometimes we don't need to communicate
outside of our teams, but in the times that we do, this can lead to some troubling outcomes.

In this post, I outline some quick tips for leading clear, effective meetings as a Data Scientist. While the post is
geared towards Data Scientists, I've tried to write the post such that the techniques can be generalized outside of
Data Science.


## Lead with the "why."
You analysis is awesome (yay!), and you want to dive right in. As tempting as it is to lead with the cool insights that
you've uncovered, lead instead with the reason for holding the meeting.

>Get people engaged right out of the gate with a clear, human-readable explanation of why everyone is in the meeting
together, and set the goals for what your team should accomplish during the time. As heavy-handed as it sounds,
**defining a “goal” in a text box somewhere on the introductory slide is often instrumental in setting up successful
meetings.**

So, why lead with the "why?" Imagine you've been meeting hopping all day, and your calendar pings you with a
reminder for a meeting in 5 minutes. Wait, what was that meeting about again? Chances are you haven't read the
meeting description since you accepted the invite a week ago. Maybe you didn't even read it then. In these cases,
it's incredibly helpful to have someone set a clear definition of the purpose and objectives right at the start, and get
everyone aligned on the meeting goal.


## State assumptions and disclaimers *before* showing any analysis.
One thing I've learned the hard way is that the second that you put a graph or a table of results in front of your
audience, you have irreversibly lost a significant portion of their attention to that visual stimuli. So, it follows
that if you're explaining important caveats and assumptions implicit in your data, people may not hear
you if you have a shiny graphic projected on the screen.

>This is where things get dangerous. Every analysis
comes with warnings and disclaimers about how to interpret, and how NOT to interpret, the results.
If the warnings aren't clear, folks can (and will) leave the meeting with conclusions that aren't true.

![danger]({{site.baseurl}}/assets/img/dragons.jpg)

It's incredibly important to present this information in a way that maximizes the chances that people hear it. For this
reason I recommend **dedicating a entire slide to detailing the warnings and assumptions implicit in the analysis,
without anything else that might distract.**


## Graphs are great! Except when they're not.
We’ve all those imposter syndrome moments during meetings where we sat
staring at a complicated architecture diagram, or someone’s modeling results, thinking “I don’t get this… man, do I
feel dumb right now” (or at least I have). This holds especially true for senior folks, who naturally feel more
pressure to be a voice of leadership in the room.

>Meetings tend to go off the rails quickly when someone feels defensive, and there is no quicker way to feel defensive
than not understanding a graph or a result.

So, practice empathy for your future audience when building your slides. For every graphic or result that you include,
review it and re-review it through the lens of “what would someone with no background in this data need to understand
this?” Are the axis labels clear? Is the graph easily interpretable?

Best yet is to phone a friend! For important presentations, I strongly recommend asking a colleague who isn't familiar
with the underlying dataset to review your slides ahead of time. Do they understand what you're hoping to communicate?


## But, don't conflate clarity and verbosity.
While we want the context and methodology to be clear to our audience, it's important not to stray into
"drowning in details" territory. Often what I need to grasp an analysis is a succinct, high-level description;
overly detailed descriptions of the precise math behind the model distract from the meaning of the results,
and will quickly lose your audience.

**I advise focusing on the *need* part of the previous question of
“what would someone with no background in this data need to understand this?”**


## Spend at least *some* time on slide design.
As a woman working in a male-dominated industry, I *still* feel slightly self-conscious when I'm tweaking the color
scheme on a slide instead of writing code. **But I'm still convinced that people are more engaged in meetings where
they like looking at the material being projected.**

>This isn't to say you need to go crazy on aligning every detail on the slide, or picking the absolute perfect font
style. But I still advocate taking a few spins through your slides, and making sure you don't lose people because
their inbox is more visually appealing than your slides.


## Phrase your follow-ups.
You just presented a clear and compelling analysis, and your audience is bought in and excited. Nice work!

This is the time where the requests for follow-up work will likely pop up. In the moment, it's easy to get caught up
and agree to a ton of new work. This topic could easily warrant its own post, but for now, I offer the following tips:

**1. Avoid language that means different things to different people.**
My favorite example is the word "easy." Technical folks typically use the word "easy" to mean "oh yeah, that is a thing
that is physically possible for us to do." Non-technical folks often use "easy" to mean "we can do that quickly." See
where communication could break down here? I have seen friction arise when an engineer described a mundane, but very
time consuming, ask as "easy" only to have a business-side consumer assume that meant the task would be fast.

**2. Manage potential scope creep with kindness.**
Don't be afraid to ask for follow up meetings to discuss an ask, rather than agreeing to it outright, to ease the optics
of publicly saying "no" to an ask from another team.


## ... and that's it!
The short version of the points above is to design your meetings, and presentations, with empathy for those who you'll
be presenting to. If you put yourself in their shoes, and aim to build material that is clear and easy to engage with,
everything else will follow.

May the force be with you, and the next amazing meeting that you lead!
