---
layout: post
title:      "CLI Data Gem Project"
date:       2019-09-18 14:55:26 -0400
permalink:  cli_data_gem_project
---



This past week, I finished my CLI Data Gem Project for the Flatiron School's Software Engineering course. The project was a culmination of our Procedural and Object Oriented Ruby modules and definitely challenged both my creative and technical Ruby skills in entirely new ways.  Gone were the days of preloaded labs and specs, suddenly I was looking at a blank text editor and tasked with setting up my own enviornment.  

![](https://junkee.com/wp-content/uploads/2017/10/internship-680x439.jpg)

I quickly realized how difficult this actually was, as I was accustomed to using Learn's IDE and didn't know where to start.  I highly recommend watching Avi's "Daily Deals" CLI Gem walkthrough video, as this showed me how to setup my local environment.  While this took quite some time, the following were some takeaways along the way. 
 
**1. Install your gem using bundler and the "bundle gem <project name>" command.
1. Create a new Github repository like this.
![](https://swcarpentry.github.io/git-novice/fig/github-create-repo-03.png)
1. Include `!/usr/bin/env` ruby to make an executable file.
1. Plan your Gem out first before getting into the technicalities of how you will code it.
1. Think about how youll will scrape your data when browsing websites. 
1. Create organized and succinct classes where you don't repeat yourself.
1. Google is your best friend!**

I thought about what I wanted to do for my project and was immediately pulled towards the idea of scraping a website for travel details.  Without much research I landed on the following [website ]

At first glance, it seemed perfect with a name, location, flight cost and hotel price that I could scrape for my Gem. However, admittedly after spending hours trying to make this website function in the way I imagined, the website did not have the appropriate html tags.

![](file:///Users/caitlinmajewski/Desktop/Screen%20Shot%202019-09-18%20at%202.11.08%20PM%202.png)

I held onto this project idea for a long time before finally deciding to pivot and restructure my idea.  I am so thankful I did because my new [website](https://www.builtinnyc.com/companies/best-places-to-work-nyc) allowed me to scrape in a succinct way and abstract my code in ways I could not before.   

It's okay to abandon your code. Holding onto something that isn't working is more detrimental in the long run.   I was able to scrape my new website in a half hour, whereas I had spent two days trying to make my original project website work. 

My advice to anyone starting the CLI Project is to spend the extra time planning out the structure of your app, even if its non-functional code.  The bones will help you add in the technical stuff and save time in the long run.  

Overall, this was unlike anything I've done in the class up to this point, testing the way I think creatively and technically. I really enjoyed working on my CLI gem and learned so much from it! 





