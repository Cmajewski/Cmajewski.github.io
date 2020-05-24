---
layout: post
title:      "Rails Associations: Has Many to Many"
date:       2020-05-23 17:22:37 -0400
permalink:  rails_associations_has_many_to_many
---


This past week I completed my Rails project, the third module project in the Flatiron School.  We were tasked with building a Rails application through complex forms, using RESTful and nested routes. 

I found that the most important step to my project was planning out the MVC relationships, specifically how my models would be associated. I began with a user story, which is a great way to clarify project scope and think about what your ideal user experience entails.

The user story is a short and simplified story of what the user wants in a new tool or additional capabilities. User stories are a way to deviate from technical development and instead put the actual user of the project at the center of the conversation.

**User Story: The desired functionailty from the user's perspective.**

In the midst of a global pandemic, I wanted a user story to focus on something that has been disrupted over the past few months, changing the way we interact with technology.  While more trivial than other concerns, I chose the fitness industry and how it has been largely disrupted during this social distancing period. Fitness companies have launched their own websites, turned to Instagram or created Youtube channels to host virtual live classes. My project would allow a user to login and see these different streaming services and schedules consolidated in one place. 

I needed a class model (or Workout to avoid naming confusion), Instructor model and a User model to start with, associating them in the following ways.  The Workout model would belong to both the User and the Instructor, as an instructor has many classes and users will take many classes.

![](https://i.postimg.cc/R02Y71C5/Untitled-Diagram.png)

However, this association didn't account for more than one user tuning in and taking each listed workout class.  To account for this more dynamic many to many relationship, I adjusted this association to a has many to many relationship. 

![](https://i.postimg.cc/QxjyJdDt/Untitled-Diagram.jpg)

Rails supports the following six associations. 

* belongs_to
* has_one
* has_many
* has_many :through
* has_one :through
* has_and_belongs_to_many

My Workout and User classes would be a has_many relationships but I needed to narrow down if it was a has_many :through relationship using a join table or a has_and_belongs_to_many relationship. I turned to the rails guide, which recommends the following.

![](https://i.postimg.cc/yd4H1CZZ/Screen-Shot-2020-05-24-at-5-24-02-PM.png)

The relationship between these two models is something I wanted to see when creating my user story.  I want a user to be able to save and book a class to their feed.  A user should also be able to look at all of the classes they have taken historically to see the instructors they liked or the class types they enjoy.  Therefore, a has_many :through relationship was the correct option between these two models.  Additionally, I could have just created a WorkoutUser join table but that relationship could also be represented through a Booking model.  I updated my model associations to account for this new association and added in a virtual Platform model, so users could also easily filter and search for classes using their favorite platform as a filter. 

![](https://i.postimg.cc/1X1wrXN3/Untitled-Diagram-2.png)

I was ready to start finally coding my project with a clear user story and correctly associated models. 

![](https://wpcdn.us-midwest-1.vip.tn-cloud.net/www.rimonthly.com/content/uploads/2020/03/GettyImages-823875020-1-768x535.jpg)






