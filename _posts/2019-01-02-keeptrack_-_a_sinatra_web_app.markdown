---
layout: post
title:      "KeepTrack - a Sinatra web app"
date:       2019-01-02 05:25:35 +0000
permalink:  keeptrack_-_a_sinatra_web_app
---



**Inspiration** – I live in a five apartment building complex in downtown D.C. with a single management and maintenance system and high service request volume.  The current system is pretty inefficient – all calls to the maintenance front desk are routed through an automated call that lists out various leasing offers for various properties all around the city; walking up to the maintenance front desk or calling them is the norm to request any repairs or upgrades; and no unique identifier is provided for seamless tracking of the request – all these factors often lead to delays in service requests being completed and definitely doesn’t make for a good customer experience.

**Proposed Solution** – Given our busy lifestyles, an online service request-tracking portal is a better way to bring issues to the management’s attention. It enables tracking throughout the entire lifecycle of the request as well as allows the maintenance issues in the buildings to be fixed early rather than snowballing into a more expensive repair. Therefore, my proposed solution benefits both the tenants and the management in short and long term. 

**Project** – My project “***KeepTrack***” allows a tenant to create, read, update and delete their service requests and is based on the Model-View-Controller (MVC) architectural pattern – separating it into three main logical components: the model, the view, and the controller. It uses Active Record for relational database management. A tenant is able to create, read, update and delete their service requests. 

The following are the requirements that were used as **guidelines** for this project - 

* Use ActiveRecord with Sinatra
* Use multiple models
* Use at lease one has_many relationship on a User model and one belongs_to relationship on another model
* Must have user accounts - users must be able to sign up, sign in, and sign out
* Validate uniqueness of user login attribute (username or email)
* Once logged in, a user must have the ability to create, read, update, and delete the resource that belongs_to user
* Ensure that users can edit and delete only their own resources - not resources created by other users
* Validate user input so bad data cannot be persisted to the database
* BONUS: Display validation failures to user with error messages

***KeepTrack*** is build with two models – tenant and request. Each tenant can have multiple requests but a request can only belong to one tenant. In order for a request to be entered, the tenant must successfully log in to the portal or sign up if they do not have an account. The web application uses validations for all the user data submitted.  If any of the login or sign up elements are missing or if the unique tenant username – password combination validation fails, the form will not submit and the tenant will be redirected to the original form. An enhancement would be  using Flash to display an error message that will appear detailing the specifics of the errors. Once the tenant is able to successfully login, they can either create a new request, edit/delete an old one or review all the requests submitted by them along with the submission date. Check out the github repo [here](https://github.com/srijakumar/sinatra-project).

Note: After I pitched this to my building management, they disclosed that they already have an online service request portal albeit poorly used. I guess the dragon to be slayed still exists ☺

