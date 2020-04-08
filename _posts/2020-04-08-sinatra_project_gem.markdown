---
layout: post
title:      "Sinatra Project Gem"
date:       2020-04-08 19:51:12 +0000
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


![https://imgur.com/C6KSHOO](https://imgur.com/C6KSHOO)


The client is the browser here that makes a request with a URL. Sinatra then uses the URL to map to a a Controller action (using routes).  The Cotroller asks the Model for data. The Model then asks the database using SQL.  Once the database returns the data, the Model wraps it into a Ruby object.  The object is passed through the controller to the view, which renders it to HTML and sends it back to the controller.  Finally, the controller delivers it to the back to the client as a response. 

The diagram here is an easier way of seeing how MVC incorporates our previous lessons and the stages of how a users request is rendered. 


**
Using MVC in Sinatra Project**

To use the MVC framework for my project, I first had to setup my file structure.  The Models, Views and Controller files all live under a larger file labeled app. 

![https://imgur.com/a/GR6bkQI]https://imgur.com/a/GR6bkQI)












