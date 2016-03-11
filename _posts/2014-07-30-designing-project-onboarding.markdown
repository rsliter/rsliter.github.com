---
layout: post
title: "Designing Project Onboarding"
date: 2014-07-30 20:03
comments: true
categories: [team dynamics, new project]
---
I've been thinking a lot about project onboarding lately.

A few weeks ago I started working on a project with an existing code base. On my first day I was able to pair-program on a bug with another developer. My pair was generous enough to use our time together to walk me through the process of setting up my workstation. We ran Puppet on my machine. He showed me a Gradle task to build the code. When it came time to run our tests, he knew all the command-line aliases to do so.

Two days later I swapped pairs to work on a feature. My new pair's workflow referenced completely different build commands and git convenience scripts.

<!--more-->

When I asked my pair about the difference between two similar scripts he wasn't sure. Just like my first pair, he had a specific development workflow, and the two hadn't worked together recently.

Lack of clarity amongst team members adds up to something larger.  Indecision between which git script to use is just one more thing a developer needs to think about during her day. Project members end up dedicating precious mental cycles to minutiae, resulting in cognitive overload.

The more time a person spends on a project, the more she begins to collect knowledge of the work. This leads to the failure of tenured team members to realize the complexity of the domain or technical stack.

<h3>Knowledge in the Head and the World</h3>

[The Design of Everyday Things](http://www.amazon.com/Design-Everyday-Things-Donald-Norman/dp/0465067107) categorizes knowledge as existing either in the head or the world. The head holds knowledge requiring initial effort to learn but can be recalled quickly once mastered. Information that you have based on outside input is "in the world."

Knowledge in the head, though slower to learn, leads to much quicker
recall once mastered.

A classic example of this distinction references a door: the placement of its handle signals to the user which way it swings open. This knowledge is held in the world rather than in the brain of a person who may need to open many different doors every day.

Individuals on my project hold much of the onboarding information in their heads. As a new teammate this means that I spend a considerable amount of time asking others where I can learn more about a given topic.

<h3>Moving from the Head to the World</h3>

Putting project information into the world is one way my team could make onboarding more transparent. We could write something defining domain-specific terms; for example, or send an email outlining the testing strategy.

There is a tradeoff between spending time building versus documenting a project. When a team is small, having knowledge in the head isn't such a terrible thing. The small team size enables the group to communicate practices and domain knowledge.

Nonexistent documentation at the beginning of a project can serve to illuminate complex processes. The need for a wiki on week two, for example, most likely signals an opportunity to simplify project context.

As a team brings new people on and loses some of its more experienced members, it runs the risk of losing key information. At this point it becomes necessary to transition knowledge out of individuals' heads and into the world, where it is accessible by the team.
