---
layout: post
title:      "TIME-MANAGE-O"
date:       2020-07-30 19:46:22 +0000
permalink:  time-manage-o
---


For my rails project, I decided to build a project management app “Time-Manage-O” that can be applied to a household/lab/store/restaurant - any situation that would require, in addition to the chore being tracked, any additional notes, lists, comments etc. This situation felt close to home as I have never been able to find that perfect planner that is not too bulky but contains enough details to document notes & comments.
It works in the following way - 
* The app will open with the option for the user to either log in (if an existing user) or sign up (if new to the app) either by email or facebook
* The app will then take them to the landing page where the following are displayed 
* 1. Chores created, if any, sorted by most recent and a brief description
* 2. All comments entered by the user
* 3. An option to create a new chore
* If the user selects the option to create a new chore, it will take them to another page where they can specify chore name, chore description, and categories associated with it
* Once the chore has been created, the user has the option to create associated tasks, notes/lists (title&content) and enter a comment they want to record as they work through that chore
* The user has the option to mark a task as completed and edit and delete chores, tasks, notes/lists and comments as they see fit.

To implement this app, I used the following models and relationships - Users, Chores, Categories, Tasks, Lists, Comments
* A user has many chores, many categories through chores and many comments through chores
* A chore has many tasks, many lists, many comments, many categories and belongs to a user
* The subparts of a chore follow in the following cascading order
* 1. A category has many chores
* 2. A list belongs to a task
* 3. A task belongs to a chore and has many lists
* 4. A comment belongs to a chore
These relationships follow a logical path of “what next do I need to successfully accomplish and document this chore”. While the aesthetics of the app can be more pleasing, it gets the work done and I intend to use it for my day to day tracking. My learning moment while working through this app was *finally* differentiating between .find and .find_by. In my head, these two database querying methods had been interchangeable but working through querying multiple sets of params values for this app, I learnt the hard (and permanent) way, they are not. .find (by id) will allow you to search for a single record (or an array, depending on the argument) in no particular order whatsoever and returns an error “ActiveRecord::RecordNotFound” if argument entered is not found. On the other hand, .find_by accepts a key value pair as a parameter and searches the data set using that and returns the first match. If no matches are found, a nil value is returned but the app will continue to function without exception. Both these methods work similarly when the record exists and is found in the database - probably the reason why I thought of them as interchangeable, but the way they handle things when the record was not found (which while working on this app, happened a bunch) makes all the difference!


