---
layout: post
title:      "Sinatra Project Gem"
date:       2020-04-08 15:51:13 -0400
permalink:  sinatra_project_gem
---


I  just completed my Sinatra project for Flatiron and am excited to be one step closer to understanding web frameworks using the Model-View-Controller (MVC) paradigm.  The easiest way to conceptualize the MVC structure was to root each component in previous course sections.


**What is MVC?**

**Model**
* The logic of your website and the connection to the database.


**Views**
* The user facing part of the website, or "frond-end" of the application. 


**Controllers**
* The connection between the views and the model, in Sinatra these consist of "routes.


![](https://imgur.com/a/h6m29AF.jpg)


The client is the browser here that makes a request with a URL.  Sinatra uses the URL to map to a a Controller action (using routes).  The Controller asks the Model for data, which then asks the database using SQL.  Once the database returns the data, the Model wraps it into a Ruby object.  The object is passed through the controller to the view, which renders it to HTML and sends it back to the controller.  Finally, the controller delivers it back to the client as a response. 

The diagram above is an easier way of seeing how MVC incorporates our previous lessons and the stages of how a users request is rendered. 


**Using MVC in Sinatra Project**

To use the MVC framework for my project, I first had to set up my file structure.  The Models, Views and Controller files all live under a larger file labeled app. The rest of the Sinatra project files are similar to labs and lessons we've used already.  The Views files contain mostly HTML, the Controller file uses "routes' to outline requests from URLs and the Models file contains our ruby classes inheriting from ActiveRecord.  Finally the ActiveRecord migration connects to our database and stores our data. 

![](https://imgur.com/a/GR6bkQI]https://imgur.com/a/GR6bkQI.jpg)

One of the bigger bugs I encountred while completing my Sinatra project was related to sessions.  HTTP is a stateless protocol, meaning each web request is totally independent of other web requests. Therefore, to store a user as logged in and not log them out every new request, the web app uses the session hash in your browser. The session hash lives in your server and can be accessed with every HTTP request, therefore we do not want any of the users information being stored there.  However, we set a user_id in the sessions to match the users ID in our database.  To do this in Sinatra and access the sessions hash in our controller we include the following code in our controller.

```
configure do
    enable :sessions unless test?
    set :session_secret, "secret"
  end
```


While, I included the code in my server I struggled to understand why my sessions_id would reset and the user_id was never saved when i'd go from one route to the next. I used a binding.pry to see this in real time and troubleshoot what was happening in my sessions hash. 

![](https://imgur.com/a/QE5x7tu.jpg)


After a User logged in I would set `session[:user_id]=@user.id` as this was the User object I just created and saved to the database. However, then I would re-route and see the following session hash.

![](https://imgur.com/s9XC9Ay.jpg)


The bug was problematic because I couldn't verify the user was signed in from page to page. The fix was simple and was just a type in my configure enable:sessions code, but showed me the importance of the sessions hash for this project.  I'm excited to build on our webrfamework understanding with Rails. 



















