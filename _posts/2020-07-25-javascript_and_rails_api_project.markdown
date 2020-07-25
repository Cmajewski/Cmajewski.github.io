---
layout: post
title:      "Javascript and Rails API Project"
date:       2020-07-25 15:01:22 -0400
permalink:  javascript_and_rails_api_project
---


For my Javascript and Rails API project, I designed an application to consolidate the many products and brands in women's health and wellness. I wanted a site where women could go to view the most popular products for that day, upvote ones they like and leave reviews for ones they've tried.

I landed on this project idea by first outlining the problem I wanted my application to answer.

### Problem: It is difficult to find the most popular product across different health and wellness brands. 

My app would parse these numerous products and offer a quick visual answer by users upvoting their favorites products. I envisioned a frontend display and functionality similar to [Product Hunt](https://www.producthunt.com/), where you could upvote products and they would move to the top of the page.

Next I began on my user story.

* A user is able to view products, add new products and upvote existing products. 
* A user is able to view a product's reviews. 
* A user is able to add a product review.

![](https://i.ibb.co/dcQPfWw/Screen-Shot-2020-07-25-at-2-39-54-PM.jpg)

I fcreated two classes for my Rails API backend, Products and Reviews, with a belongs_to and has_many relationship.  Products have many reviews and all reviews belong to a Product. 
 
 
