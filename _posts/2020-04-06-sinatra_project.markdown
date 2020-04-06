---
layout: post
title:      "Sinatra Project"
date:       2020-04-06 04:24:37 +0000
permalink:  sinatra_project
---


For my sinatra project I decided to utilize my favorite thing to collect, sneakers.
The application is intended to help users keep track of their current sneaker collection
and how many pairs they own. A big part of making this app worth it for me was adding a photo to make
the user's experience more elegant. This allows the user to easily view their collection
and make selections based on their current outfits without having to go through all their
boxes.
Setting up everything was pretty seamless thanks to the Korneal gem. Once a
new file was created, everything was set up and ready to receive the logic. The
problems began with the convention of RESTful Routes. The more routes added, made
it hard to keep things organized. Aside from which, it made it harder to add features
without disrupting the flow of the app. Because of time concerns, I decided to scale
back my vison on the features for the app. However, it does meet the minimal
requirements for this project. a few features like search for sneakers by user or ordered
list would have made this app a bit more updated.
I struggled planning out what attributes were needed for my sneakers so I set
up some basic, generic attributes to get me started. Once my sneaker migrations were
all complete, I used sinatra's RESTFulRoutes to start adding and displaying the
information for my sneakers. Once I got them to display it was time to set up my users. I
created a user table and set user to has_many sneakers. However, I continued to get all
sneakers instead of the sneakers for the logged in user. After setting up a current user
everything felt more connected. Once the skeleton of my MVC and  was set up I used the
remaining time to make my app more aesthetically pleasing and user friendly.
