---
layout: post
title:      "My rails application"
date:       2020-05-15 08:56:51 -0400
permalink:  my_rails_application
---


For my rails project I decided to build an app called “Talk Show”. Talk Show is an app where users come together and discuss their favorite TV shows. I am not an avid TV watcher but with the current situation, I have definitely come binging new shows. I faced many challenges with this project, but overall I am satisfied with the results.

  I started my app by creating a chart which mapped out how my users would be associate with TV shows through comments. I then used the devise gem to handle my authentications, which was a solid next step. I then created the models for my comments and TV shows. I struggled with the associations, mostly because TV show was spelled slightly different dues to snake case. But the hardest part overall was using omniauth, because the lesson doesn’t explain how to authenticate through devise. So I had to learn devise in order to learn how to make my omniauth work. 
	
	```     resources :tv_shows, path:"recent_tv_shows_path"  do 
      collection do 
        get :recent
      end 
    end
   resources :tv_shows, path:"most_comments_tv_shows_path"  do 
      collection do 
        get :most_comments
      end 
    end
		```

A Collection is a way to create a custom route within an already defined set of resources. I believe its named collection because of the additional route added to the collection of routes. The name collection references the collection of routes created by resources. Collection routes are used for functions/features such as search. A form would normally default to a post method rather than a GET. Collection helps Rails to recognize paths such as /TvShows/search as a GET request, and route to the search action of TvShowsController. It will also create route helpers, and all of the restFul routes (new,show,edit, update & destroy). I assumed that because I would be adding a search feature that it would be easiest to operate on a collection for future updates. Collection routes are established for actions performed on a collection of the resource (in my case tv_shows). In reference to my app I am using collection to search the collection of tv show reviews. I honestly did not need Collection to make my app operational, I could have created a custom route and rendered it on the index page. But my current order does help make future changes more organized and easier.

