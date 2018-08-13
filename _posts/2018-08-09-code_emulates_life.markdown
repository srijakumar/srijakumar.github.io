---
layout: post
title:      "Code emulates life"
date:       2018-08-09 17:16:25 -0400
permalink:  code_emulates_life
---


##### Introduction:
Code emulates life. With Flatiron Full Stack Web Development, I have seen this reflected in multiple ways. CLI Data Gem is the first project where I got a chance to apply different aspects of programming that we learnt in different discrete sections. We learnt how to interact with the classes, differentiate between different types of methods, apply scraping to get pieces of a website – all in the safe environment of their specific sections following the material. The learning was more focused and streamlined – we did not have to delve into the stack of all new information to choose which notecard to pick out. This data gem allowed me to do that. Very similar to real life where one learns the differential equation in the math class, Newton’s laws of motion in the physics call before combining it all together to build a single rotor helicopter.

##### Idea:
In those copious lines of instructions on this project, I grabbed onto something that sounded familiar – scraping. Okay, I had recently finished a lab about scraping, which felt familiar. Living in the heart of politics, I decided to scrape the Washington Post website to display the 5 most read headlines to the user. The user could then select one of five article headlines to display the complete article. That was the idea!

##### Process:
Now let’s talk about the process. The first thing I wanted to determine was that this website is “scrapable” (so to speak). Scraping is exactly what it sounds like. You pick and choose (or scrape) the pieces of the website for your own personal/business needs. Have you ever found yourself shuffling between two or more websites and thought “Man, I wish I could pick and choose the certain aspects of these websites together in one place!”. Well, look no further, scraping to the rescue!

Once I had decided on the “parent” website, I needed to confirm that this website had specific identifiable tags associated with the news headline, author and the article that I wanted to display to the user.

As you can see, it was pretty easy to locate the 5 headlines are neatly wrapped in “.skin” tag.

--image--
 
 

I drilled down and I found clear pathways to the url and the title of each articles

--image--
 



 

And, I used a loop to iterate over and gather the title and url of each of these 5 most read headlines.

--image--

 

That was promising! Then I delved a little deeper to see if it was possible to gather the author and the description for the article in case the user would like to read the entire article in the app itself without leaving to go to the Washington Post website.

I found that each author had the same a span[itemprop = "name"] tag and the article body was stored in p[data-elm-loc] tags. I could set p[data-elm-loc = “1” or “2” or “3”] depending on the paragraph I wanted to read. I decided to not specify it so that I can display the entire article in my app.


 --image--
 

This provided me with the core information on how to create my application. I built on these to create my CLI where the user is presented with the 5 most popular and has the option to choose any headline to read the entire article or simply exit until next time.

##### The Future:
There are multiple ways I can enhance this application! A 2.0 version of this app could allow a user to enter the zip code and see the top most read headlines from the local newspaper. A 3.0 version could allow the user to view the top headlines in specific categories. The list is endless. All I need is more skills on how to build them!

