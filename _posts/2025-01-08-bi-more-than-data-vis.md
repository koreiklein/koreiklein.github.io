---
layout: post
title: "How Business Intelligence is More Than Just Data Visualization"
date: 2025-01-08 14:10:23 -0400
categories: 
---

* Do not remove this line (it will not be displayed)
{:toc}


## Quodor Data
Here's another post in a series I'm doing on topics related to the new Business Intelligence (BI) tool I'm working on called
[Quodor Data](https://www.quodor.com/quodor-data-demo-video).  This post explores the ways in which a BI tool is doing
more than simply creating visualizations of data.


## Isn't Data Visualization Enough?

I remember when I first encountered BI tools, I was kind of perplexed as to what they did that I couldn't already
do with a data visualization tool.  If you already have python and matplotlib, then you can make all the charts
you need, no?  Same goes for Google Sheets / Excel.  So what's the point in paying for a tool to make some bar/line charts
that you already make using tools you already have?

At the same time, every company I've worked for has relied heavily on a BI tool.  I hear about nearly every tech startup
eventually shopping around for its BI tool.  I also see reports estimating the total size of the market for BI tools
in the billions or tens of billions of dollars (depending on how you count).  Presumably, there must be some reason
people spend all this time and money on BI software?

### Where Data Visualization Falls Short

To put it as concisely as possible, ordinary data visualization tools don't attend to the social and collaborative
needs an organization has around visualizing its data.

To give an illustrative example, let's say I'm working on software for a laboratory and I want to understand how much
time is spent on each stage of the lab's experiments.  I could put together an excel sheet with some charts or a python
program to visualize the data for me, and then I'll personally understand the answer to my question.
Now suppose I want to get other people involved.  Maybe there's another coworker that's looking to find ways to cut
back on how much time we spend doing each experiment, and so they want to see the same results I put together.  Do I
send them a handful of PDFs?  Maybe I can send them the python script I used, or the spreadsheet, but then what if they're
not technical enough to know how to make simple changes?  I'll probably get peppered with requests to make super simple
changes to the charts e.g. "can you redo charts, but just for experiments run by so-and-so's team?" or "these charts
are three weeks old now, could you please update them with the most recent data?" or "you're only displaying a month of
data here, could you make it cover the past two months?"  If you've ever released some kind of data report to business
users in PDF form, you've probably encountered a ton of these kinds of requests.  They're all kind of small, but collectively,
they can start to take up all your time, to the point where you're too distracted to make progress on any of your other
projects.

## Features of The Business Intelligence Tool's Approach

BI Tools are designed to visualize data in ways that are most valuable to the organization as a whole.  This means they
have to get a number of things right:

#### BI tools produce reports that are easy to digest. Even without any technical expertise.
A BI tool should be able to produce a dashboard so straightforward that you can forward it to anyone in your organization and they'll be
able to get a rough sense of what the data is showing immediately and without any coding or technical know-how.  Maybe
you might need to talk them through what some of the charts mean, but if your BI tool has a good enough AI assistant, the
assistant should be able to answer those questions for you.

#### Nontechnical users can tweak simple parameters to modify reports in predictable ways.
The reports in a BI tool are easily configurable.  Typically, the end consumers of the data can set some kind of
`start_at` and `end_at` parameters to indicate the time period they're interested in, and all the reports will automatically
restrict themselves to just that time period.  A good BI tool will let you include pretty much any other parameter you
can dream up e.g. you release an "Experiment Detail" dashboard for people in your laboratory that gives a complete
overview of any one experiment, and it comes with an `experiment_id` parameter that they can change to select the particular
experiment they're interested in.

#### BI tools keep their reports up to date
You don't need to take the time to re-run reports in your BI tool.  The reports should simply always be using the most
recent data.  This feature is a tricky thing to implement, and it means the BI tool should have some kind of
[pipeline management](https://koreiklein.github.io/2025/01/01/why-bi-needs-pipeline.html) features built in.

#### The List Goes On
The features above are some of the most important, but depending on the particular BI tool, there are a whole
host of other things they might offer.  We're not going to get into all of them here, but for the most part, they
tend to be features that somehow support or enhance one of the above three.

## Use Cases Enabled by a BI Tool
The above list of features is enough to support using a BI tool within an organization for things you couldn't otherwise
do with simple data visualization tools.  Here are couple common ways I've seen organization make use of their BI tool:

#### Creating Alignment
By far the most impactful use I've seen for BI tools is when they help create alignment between different parts of
an organization.  It's very easy for different teams to use different sources of data and wind up with different
and incompatible views of what's happening.

To give one example I know quite well, in a logistics organization,
you can have several teams that all care deeply about the time it takes between when goods first arrive in the country
until they're first available to sell to consumers.  That delay is one of the most important metrics to the organization
and everyone uses it in a different way:  The operations teams set targets on how much delay they're allowed to introduce
and regularly compare their performance to the target.  Process engineering teams 
have to understand where to find the major opportunities for improving that metric by modifying company processes.
Marketing and sales teams need
to communicate about that delay to customers and set proper expectations on how long they'll have to wait for goods  
to move from place to place.

Generally, almost any organization benefits from keeping different teams and stakeholders aligned on key pieces of
quantitative information, and a BI tool can easily be instrumental in creating that alignment.  In the example above,
the company should release a BI dashboard that displays the "official" record of how much delay there is in moving
goods from start to finish, and every team works off that same dashboard.  If someone wants to exclude outliers, or
process/interpret the data differently, they propose and release a change to that one dashboard, and all the different
stakeholders stay in sync about the changes to their data.

#### Structuring the Weekly Metrics Review Meeting
Some organizations are extremely metrics driven; each team lead is made responsible for certain key business metrics
and needs to report regularly to peers and to upper management about a) how are those metrics looking, b) are there any
notable changes or causes for alarm and c) what's the team doing to improve those metrics.

Organizations like this are quite fond of the weekly (or monthly / quarterly) metrics review meeting.  This is usually
the meeting at which teams present on their metrics.  To prepare for such a meeting, the manager will need to put together
a quick presentation, complete with tables, graphs, bar/line charts.... basically everything a good BI tool should be
able to maintain for you.

An organization that's making the best use of their BI tool will integrate it thoroughly into the metrics review meeting.
Maybe each team gets their own BI dashboard for reporting on metrics.  Certainly, the BI tool can reduce the amount of
time the team leads have to spend preparing for the review meeting.  I've seen teams spend a day or more before each
weekly review meeting just rebuilding the same charts they use every week.  The BI tool can spare them all that time,
and help them devote more time into understanding the root causes of new trends and anomalies in their data.

#### Connecting Individual Contributors to Company Goals
Individual contributors within an organization function much better when it's clear how the work they do
contributes to important company goals.  When a manager assigns a project to one of his reports, he should make it
super clear exactly how that project is supposed to be good for the organization.  In particular, it's best if the assignee
knows exactly which important company metric is supposed to improve as a result of the project.

Especially for more senior contributors, assigning them a project explicitly devoted to improving a particular business
metric is one of the best ways to unlock their creativity.  Rather than spelling out exactly how to proceed with the project
the manager gives autonomy to the contributor on what to do, but still holds them accountable to the goal
the company is ultimately looking to achieve.

One common pattern is for the contributor to start off with the metric in the BI tool, and make for themselves a project
specific dashboard to show everything relevant to how they want the metric to improve.  Maybe they put the metric
everyone else cares about on the top of the dashboard, and beneath it they put all the other reports that are specific
to the particular approach their project will take to improve it.

## Want One?
The above discussion covers what I think are the most compelling reasons a company should want to start using a BI tool
for visualizing their internal company information.  I went through the major features they have that simple data
visualization tools lack, and the kind of use cases those features unlock for you.

If you're considering shopping for your first/next BI tool, please don't hesitate
to [get in touch](https://www.quodor.com/quodor-data-demo-video).  Quodor Data is working on a tool expected to launch in
2025, and happy to refer you to another BI tool if you have different needs or a different timeline.
