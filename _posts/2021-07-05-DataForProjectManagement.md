---
layout: post
title: "Moneyball for Project Management"
date: 2021-07-05
published: true
---

Have you seen or read Moneyball?
<iframe width="560" height="315" src="https://www.youtube.com/embed/rgXESVtWX3U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>

I love this scene in the movie. It's when Billy Bean's analytical style of building a baseball team first runs into the old-school wall of "expert" knowledge. Project Management today is the old scouts in the scene. We talk like we're experts and have everything figured out, but it's mostly just hot air - with no data to back up our positions or justify our practices. The Houston Rockets and the Oakland A's take data more seriously than companies that claim to be at the forefront of engineering. I've been involved in project management for nearly twenty years. What counts as good project management hasn't evolved at all. Twenty-four year old me could step into 2021 and recognize all the tools<sup>[1](#tools)</sup> and processes used today. That's not a good thing. Project Management<sup>[2](#pm)</sup> desperately needs to find it's [Billy Bean](https://en.wikipedia.org/wiki/Billy_Beane). When baseball and basketball started taking a serious look at data, the sports realized their long held assumptions about how to play the game were wrong. Today both sports are played very differently then they were ten to fifteen years ago<sup>[3](#style)</sup>. I think it is very likely Program Management could undergo a revolution of this magnitude as well if we would start using the data around us.

So how do we bring Moneyball to Program Management? I think it's at least three steps<sup>[4](#standard)</sup>: Identifying the opportunities for harvesting the data, standardizing how that data is formatted so that it can be collated at scale, and finally analyzing the data. The field of data science has burst on to the scene in the last decade. A requisite for this to occur was the avalanche of data that our networked world has made available to us. Data science and machine learning work best when they are presented with large amounts of data. Amounts that were not available in the past. I haven't seen any effort in the area of project management to collect data at the levels required to use modern data science/ML and then explore uses for that data. Below are some of the opportunities that I think about.

# Harvesting the Data

Identifying the most useful sources of data is the first step. Some of these sources often already exist, others might need some work to create.

## Timekeeping

This is the most obvious opportunity and the most egregious case of neglect. At least in companies that have defense contract business, detailed data is collected data by each person on what projects they have worked on 
each day, and how many hours they worked on them. Unique charge codes are given to projects, and often projects inside of projects. That data is uploaded into some database. The reason this data is collected is for the US government and the company to agree on rates to pay by the hour on government contracts, but it can be used for other purposes as well. Type of data that is in every entry in the database usually includes:

* Project Code - what project the time is being charged to.
* Date - What day the hours were applied to the project code.
* Cost - The cost of the hours
* Skill - Typically the person applying the hours has been assigned a skill (e.g. design, analysis, purchasing)
* Person - The name of the person charging.
* Department - The organization that the person belongs to.

## Part Trackers

I have experience at two (admittedly very old-school) aerospace companies. My experience with these two is very 
consistent. When new programs require even a moderate number (~ 15 or more) of parts to design and make, some type of crude (usually Excel) type of "parts tracker" is created. The parts tracker keeps track of things like:

* The status of new drawings for parts.
* When orders are placed for new parts and for how much.
* Part quantities on hand (from which shortages can be calculated)
* Expected delivery
* Instrumentation status

One might ask why this information isn't track of in the enterprise wide databases that large companies have that keep track of similar data on programs in production? The reason has been that the bureaucracy involved with adding data to these databases is too onerous to move with the speed and low overhead that is needed for new product development.

## Meeting Notes

It may be able to parse program's meeting notes with Natural Language Processing (NLP) to gleam data regarding a program's status and health. This is part of why I've been keeping my team's meeting notes in flat text files. Using the note tracking tool that I wrote about in a previous [post](https://sgtaylor16.github.io/2020/03/29/Notes.html)

## Milestone Trackers

Wouldn't it be great if we could use milestone trackers for something besides making people feel bad about themselves? It seems we only use milestones to use against people at performance review time. Ask anyone where the milestone results are for past years you won't get anything useful back. It's possible milestone history can be used to measure the success or failure of changes to PM practices over time. This can only be done if milestone history is saved year-over-year.

# Organizing the Data

As were figuring out what data we want to collect we need to think about what formats we store it in so that we can use more easily use the data with modern data science tools. Storing files in proprietary formats like MS Office products makes getting at big data very difficult. Ways should be found to store data in flat text files at a minimum, maybe databases for larger data stores. This is not new ground. People working in data science have to think about this on a daily basis I think.

# Using the Data

Assuming we identify good potential sources of data, and collect the data in a way that makes the data easy to use, we still need to analyze the data. But that's the fun part. If we have the discipline to execute the first two steps, there's little doubt that people will analyze the data in many different useful ways. Studying data generated from real projects may help us understand how large projects really develop. The main way we describe projects today is with Gannt charts. Gannt charts are very useful, and I wouldn't want to give them up. But Gannt charts do not capture the real chaos in any large development program. Task B does not actually start cleanly when Task A is neatly completed and I would guess a fair fraction of the work that is completed in a program never had a clear home in the Gannt chart shown to management or the customer. Looking at historical data through a lens other then Gannt charts may help us understand patterns in how resources are expended to complete tasks in real life. Learning from this exercise may create new ways to estimate new projects or monitor the health of existing ones.

<br>
<br>
---
<br>
<a name="tools">1</a>: Powerpoint and Excel, maybe with macros.<br>
<a name="pm">2</a>: When I mention program management. I mean program management for complex physical projects. Think rockets, planes, cars. I do not mean software project management which may or may not be similar - I don't know.<br>
<a name="style">3</a>: I am not making a statement on the entertainment value of the new styles. I miss post play in basketball and baseball is even more boring than it was.<br>
<a name="standard">4</a>: I don't think these steps are profound. Any new problem that wants to use it's data probably uses something like this without thinking about it.