---
layout: post
title:      "Rails Associations: Has Many to Many"
date:       2020-05-23 17:22:37 -0400
permalink:  rails_associations_has_many_to_many
---


This past week I completed my Rails project, the third module project in the Flatiron School.  We were tasked with building a Rails application through complex forms, using RESTful and nested routes. 

I found that the most important step to my project was planning out the MVC relationships, specifically how my models would be associated. I began with a user story, which is a great way to clarify project scope and think about what your ideal user experience entails.

The user story is a short and simplified story of what the user wants in a new tool or additional capabilities. User stories are a way to deviate from technical development and instead put the actual user of the project at the center of the conversation.

***User Story: The desired functionailty from the user's perspective. ***

In the midst of a global pandemic, I wanted a user story to focus on something that has been disrupted over the past few months, changing the way we interact with technology.  While more trivial than other concerns, I chose the fitness industry and how it has been largely disrupted during this social distancing period. Fitness companies have launched their own websites, turned to instagram or created youtube channels to host virtual live classes. My project would allow a user to login and see these different streaming services and schedules consolidated in one place. 

I needed a class model ( or Workout to avoid naming confusion), Instructor model and a User model to start with, associating them in the following ways.  The Workout model would belong to both the User and the Instructor, as an instructor has many classes and users will take many classes.

https://imgur.com/a/wWZxOSO

![](https://imgur.com/a/wWZxOSO)







