---
layout: post
title: A Primer on Developing Data Pipelines with Django (with puppies)
date: 2019-08-06 13:32:20 +0300
description: A primer on developing data pipelines in Django
img: puppies.png
tags: [software development, tutorials, Django, Celery, data pipelines]
---
Data Science work typically falls into two main categories:
1.  One-off analyses that we develop on our local machines, present to our stakeholders, and (in most cases)
never look at again
2. Analyses that we run repeatedly, often in a production environment

Often when we're working on a project in the latter category, we'll need to do at least some data pipeline development.
Maybe our automated analysis needs to interface with other software systems; maybe we need some queueing mechanism for
analysis tasks; or maybe we need to store the results of our automated analyses somewhere accessible and robust. These
are all cases where we'll likely build out data pipelines.

In this post we'll design, build, and test an automated data analysis pipeline as a Django microservice. We'll focus on
a use case and related data centered around one of my favorite topics: puppies!

Note that this is not intended as a deep dive into Django or microservices, but rather as a high level case study of
how we can leverage Django for automated analysis projects.

--- work in progress, to be continued ---
