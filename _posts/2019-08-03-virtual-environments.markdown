---
layout: post
title: Python Virtual Environments, Tea, and You!
date: 2019-08-03 13:32:20 +0300
description: # None for now.
img: tea-cup.jpg
tags: [virtual environments, tutorials]
---
Recently I've been consolidating the things I wish I had known about when I was getting started in the field of data
science. One of those things is - you guessed it - virtual environments in Python!

This post is intended as a gentle introduction to virtual environments for Data Scientists of any level who want to
improve their development environment game (and read about tea, of course).

## 1. What is a virtual environment?
If you Google search "what is a Python virtual environment" you will find something along the lines of "a tool to
create isolated Python environments." This isn't a particularly clear definition, so let's talk about tea.

Imagine you invite a friend over for tea. You decide to make chai tea and brew up some black tea, cloves, cinnamon,
and ginger. You add some whole milk to your tea and, remembering that your friend is lactose intolerant, add soy milk
to his cup instead.

We can see that because you and your friend have different dietary requirements, you need slightly different tea
recipes. You each have the same "version" of tea and spices, but different "versions" of milk. In this case, adding the
wrong "version" of milk to your friend's cup would have unfortunate consequences for him!

> **How is it that you and your friend, with very different dietary requirements, are able to enjoy tea together?
The answer is that the teacups allowed you to add different versions of ingredients to your own personal teacups.**

![tea-cups](/assets/img/tea-cups.png)

What the **teacups** are to you and your friend, **virtual environments** are to Python projects with different
requirements.

## 2. What is a virtual environment? continued - bringing this back to software
Like you and your friend, Python projects often have different requirements. Projects depend on specific packages, and
on specific versions of those packages. So how the heck do we work on projects with different requirements, if we only
have one computer?

> **Virtual environments allow us to maintain many development environments (tea cups) with different packages
(tea, spices, milk) and different versions of packages (black versus green tea, milk versus soy milk, etc), where the
environments know nothing about each other and are completely isolated from each other, on the same computer.**

## 3. Why virtual environments are awesome: collaboration!
Most tutorials on virtual environments focus on the benefits of keeping your personal local development space clean and
free from painful version-ing conflicts. This is absolutely true, but it misses one of the most important benefits
about virtual environments: they **enable stress-free collaboration between developers and/or data scientists.**

<img src="/assets/img/tea-party.png" width="500" height="344" style="float: right;margin-right: 10px;margin-top: 7px;">

Let's say you're working on an awesome project on your local machine, and decide that you want to collaborate on it with
a friend or a colleague. To do this, your collaborator needs some sort of information about how to replicate the
required packages and versions that you used for the project. If they don't have this, we're likely headed down the
frustrating detour of sorting through missing packages, version conflicts, etc.

We will pass on the information about what packages and which versions she'll need via the _requirements.txt_ file. If
you haven't heard of this before, I recommend skimming this [awesome article.](
https://medium.com/@boscacci/why-and-how-to-make-a-requirements-txt-f329c685181e) Your collaborator can then
clone your repo, create a new virtual environment, and install the requirements listed in the requirements.txt file.

> **The beauty here is that even if your collaborator has packages installed which are different versions from those
specified in your requirements file, the new virtual environment that she creates will let her install
all of the required packages in an isolated environment without conflicts or dependency issues. Awesome!**

## 4. Okay, I'm in. What options are out there?
At the time of writing this tutorial, four of the most popular options are:
* `venv`
* `virtualenv` (yep, this is indeed a different package from `venv`!)
* `conda`
* `pipenv`

It's worth noting that each of these has its own advantages, and its own drawbacks. If you're getting started at a new
job, I highly recommend checking with your team to see if there is a standard or common practice for virtual environment
management at your company.

## 5. Opinions, everyone's got 'em: a case for using venv as a Data Scientist
<img src="/assets/img/tea-cup-colors.png" width="350" height="290" style="float: left;margin-right: 15px;margin-top: 7px;">
My strong personal preference is to use `venv` to create and manage virtual environments (especially if the project is
being deployed to production).

A side note in favor of `conda` is that many popular data science Python packages have C or C++ dependencies, which can
be tricky to deal with. `conda` takes the headache out of the process because it handles [packages written in any
language](https://www.anaconda.com/understanding-conda-and-pip/) (not just Python).

However, assuming that you're not working on a heavy duty machine learning project, `venv`
is my vote. I'll follow up with details in a later post, but the short version is that a lot of the complexity-driven
drawbacks of `conda` and `pipenv` options aren't a problem in `venv`, given that it was added as a standard Python
package in Python 3.3

## 6. Getting started with venv
Alright, now that we've gotten through the primers, the real fun begins! Open a terminal, and follow the steps below
to create your virtual environment in `venv` (note that these are written assuming macOS):

1. Create a new project, or `cd` into the root of an existing project that you'd like to create a virtual environment
for.
2. Create a new virtual environment: `python3 -m venv venv`. Note that: (1) `venv` is included in python3 by default so
there is no need to pip install anything, and (2) that last venv is just the name of the virtual environment (we can
name it anything we like, such as `python3 -m venv chai_tea`; the name "venv" just keeps things clear).
3. Open up your project in your IDE; you should see a new directory in your project called `venv` (or whatever you
named your new virtual environment). Nice work! (also, we can see that a virtual environment is really just a directory
containing scrips - not so scary after all!)
4. Activate your new environment: `source venv/bin/activate` (again, swap out the "venv" part for whatever you named
your environment, if you named it something different)
5. You should now see `(venv)` in the far left of your terminal screen.
6. Before installing packages (either for the first time, or from a requirements file), we'll want to make sure that
we are on the latest version of pip: `pip install --upgrade pip`
7. If you have a requirements file that you would like to build from, run the following: `pip install -r requirements.txt`
8. Alternatively, you can now pip install the packages you need by hand if this is a first-time build. Once you're done,
add your requirements and their versions to a requirements.txt file (you can always run `pip freeze` to check versions)
9. If this is a git repo, we'd like to _not_ commit the virtual environment (your collaborators will be able to create
their own and load the requirements from the requirements.txt file). So, add a line with just the text venv (or whatever
the name of your virtual environment directory is) to your .gitignore file.
10. To get back out of the environment, simply enter the command `deactivate` - you'll notice that the `(venv)` on your
terminal screen goes away to let you know you're "back to reality!"

## 7. And that's the tea!
Takeaways from this tutorial:
1. Virtual environments are a powerful tool for keeping your local development environment flexible, and for
collaborating with other data scientists / software engineers.
2. `venv` is my top pick for creating and managing environments, but in the case of projects with C-dependencies (see
many of the SciPy packages), `conda` is a good alternative.
3. `requirements.txt` files are your friend (if not using `pipenv`).

Thanks for reading, now go reward yourself with a cup of tea for making it through the tutorial!

![tea-party](/assets/img/tea-mood.png)
