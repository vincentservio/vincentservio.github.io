---
layout: post
title:      "My Final Projext"
date:       2020-10-17 17:48:45 +0000
permalink:  my_final_projext
---


Going into this project for me was very bitter sweet. Although i was happy to reach my final project, i was sad to know that all of the fun throughout the process was coming to an end. I didnt exactly know what i wanted to build when i started my project becauase i still wasnt comfortable with the flow of redux.I chose to build a Song tracker to help orginize thoughts for artist. My application takes in a title, instrumental, notes/lyrics, and a status. The information is later used to display in a fun and orginized manor. 

I had tons of fun working with React Components. With a really strong grasp of javascript, React felt like a seamless transition. One thing that i did struggle with was knowing when to use a funtional component vs class components.Class components can be used in every component and function properly. In fact if one is unsure on which component to use, it is a good idea to start off with a class component. However A Functional components do not go trough a series of checks related to its lifecycle.  In result if we do not need state or lifecycle methods, we can just use a Funtional comoponent. Funtional components returns JSX, unlike a class container which uses render.  Functional components does not exented Component so it does not store state.    

Redux is a predictable state container. Using Provider, redux allows access to state from any nested components. I didnt struggle much getting Redux set up. However I didnt clearly undestand the flow and how data was passed into the store.After building out a few models, I console.logged through every step.  Here's what i found,  an action creator creates an action. The action gets fed to dispatch which then feeds the information to the reducers. The reducers takes in two arguments, current state, and the action. The reducers creates a copy of current state,  and  utilizes that information to create a new state. Once i understood how the flow actually works, it was fun to add more features to my app. 


