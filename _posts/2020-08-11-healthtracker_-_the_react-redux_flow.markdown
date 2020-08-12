---
layout: post
title:      "HealthTracker - The React-Redux Flow"
date:       2020-08-12 03:37:30 +0000
permalink:  healthtracker_-_the_react-redux_flow
---


For my final React project, I built a habit tracker app which can be applied to any other non-health habit tracker as well. The inspiration for this app was COVID19 quarantine during which my normal routine was thrown off balance and as they say - “man is a creature of habit”. So cue crazy sleep hours, waking up just in time for work, brushing teeth at night, dessert for breakfast - you get the drift. I wanted to create an app which is simple to use and gets the job done. 

Let me give you a walkthrough of the app - the user will create a tracker for the habit they want to track. It can be anything such as “8 hours sleep tracker”, “watered the plants daily tracker” or “did not eat sugar tracker” (I really needed that last one - thanks, COVID19!). Once the user has created the tracker, they will find the newly created tracker from the list and click on it which will take them to the individual tracker page. Document the days they worked towards that goal with a note, if that helps as notes are optional, while making sure to enter the date in "yyyy-mm-dd" format due to system restrictions. Now, they can watch the trend in the calendar associated with the tracker! Additionally, the user can modify tracker names or delete the notes as per their needs. To gamify a bit, they can also click on the "Most Popular" button to see which habit they have been working on the best! 

While working on this app in React along with Redux, I often found myself referencing the concept notes around Redux and found that dataflow extremely confusing. Now that I have given an overview of the app, I would like to quickly touch base on these concepts in hopes that if you are running into issues due to the terminology and dataflow, this blog helps! First is Provider - this is something that wraps your entire app or the outermost container of your application. Store - is the data center of the entire app and controls the Provider by setting constraints. Store will contain the Reducers that can modify the Store and are in turn activated by Actions. So if you’d like to add an additional tracker to the Store, you’d need to have an Action that signals adding the tracker that will then initiate the Reducer that does the actual job of adding the tracker to the Store. While there are various other nuances associated with Redux, getting a grip on these provided me with the basic data flow understanding that can be built upon depending on the need of your project!

