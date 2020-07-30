---
layout: post
title:      "DiveTracker"
date:       2020-07-30 19:42:01 +0000
permalink:  divetracker
---

For my JavaScript project, I decided to build a dive tracking app “DiveTracker”. I am dive enthusiast and to maintain my PADI certifications, I have to ensure I have a certain number of dives along with the details associated with it to avoid retaking a less-fun skills dive. 

With this app’s frontend, a diver can note down the dive by assigning a title, date, details such as location, depth, currents, visibility and the marine lives observed. In case multiple dives were undertaken on the same day, the different log details and observations can be entered and assigned to the day along with the option to delete the log/observation should the user desire.

This was achieved on the backend with the help of three models - day, logs & marine lives, and the associated controllers. The day model has a one to many relationship and follows the logical path of what all do I want to record to maintain my certification status and remember the day. This is a basic version and there are various improvement opportunities that this app affords - 
Allowing a user model to curate the logs & observations to a specific user
Allowing the user to invite their dive buddy to contribute any dive pictures/comments/edit details pending user’s approval

Working on this app while making sure it was a single page application led me to write a lot of HTML in the JS file which had its own share of tedious review whenever something didn’t display accurately. So in addition to a dive tracker, I also got meticulous combing through the code skills down and hope to continue to refactor it to avoid repetitive code.


