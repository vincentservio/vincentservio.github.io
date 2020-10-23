---
layout: post
title:      "My Final Project"
date:       2020-10-17 13:48:46 -0400
permalink:  my_final_projext
---


Going into this project for me was very bittersweet. Although I was happy to reach my final project, I was
sad to know that all the fun throughout the process was coming to an end. I didn’t exactly know what I
wanted to build when I started my project because I still wasn’t comfortable with the flow of Redux. I
ultimately chose to build a Song tracker to help organize thoughts for artist. My application takes in a title,
instrumental, notes/lyrics, and a status. The information is later used in a fun and organized display for
the user.

I had tons of fun working with React Components. With a really strong grasp of javascript, React felt like a
seamless transition. One thing that I did struggle with was knowing when to use a functional component
vs class components. Class components can be used in every component and function properly. In fact if
one is unsure on which container to use, it is a good idea to start off with a class component. However
functional components do not go through a series of checks related to its lifecycle. In result if we do not
need state or lifecycle methods, we can just use a Functional component. Functional components return
JSX, unlike a class container which uses render. Functional components do not extend component so it
does not store a state.    

Redux is a predictable state container. Using Provider, Redux allows access to state from any nested
components. I didn’t struggle much getting Redux set up. However I didn’t clearly understand the flow
and how data was passed into the store. After building out a few models, I used a console.log and debugger to understand and walk through every
step. Once i got the grasp of the flow of redux, I started to make undetstand why these princeples are in place. An Action is simply an object that has a type field. That action is created and retured through a function called an action creator. The only way to update state is to call  dispatch which  takes in the  action object . The store than takes that action and passes it to the reducer. The reducer takes in initial state and action, makes a copy of state, decides whether state should be updated and return new state based on the action type. After the store than waits for another action. Once I
understood how the flow actually works, it was fun to add more features to my app.




