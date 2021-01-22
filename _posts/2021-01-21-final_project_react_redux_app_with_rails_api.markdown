---
layout: post
title:      "React/Redux Concepts in Layman's Terms"
date:       2021-01-21 21:05:38 -0500
permalink:  final_project_react_redux_app_with_rails_api
---


For this blog, I wanted to cover the topics that I came across as I was introduced to React/Redux: mapStatetoProps and mapDispatchtoProps. But first, l'd like to go over basic ideas behind Redux, to better understand the previously mentioned functions.

Why **Redux**?
As we know, in React, components come with a built-in state object, where you can store its values. However, as applications get larger and more complex, and we have more and more components, we then start getting a complex web of properties and state that becomes difficult to work with. With Redux, we can store all of the necessary data in our application in one place, one state, one JavaScript object separate from our components.

Where is this Javascript object you speak of, with the entire state?
A **Redux "store"** stores the entire state of the app in an object. To create a store, we use the createStore function.

How does a Component get access to the store, with the data it needs?
There is a special package specifically for connecting your redux store to your React. **React-Redux**.  You must import this into any component that you will connect to redux. Then you use the middleware:  **Provider**, which makes it so that your entire application can access any data it needs from the store. We then use the **connect()** function from React-Redux, and supply a **mapStateToProps** function to pull out the data you need.

mapStateToProps? What is that?
As the first argument passed in to connect(), mapStateToProps is used for selecting which part of the data from the store the connected Component needs.

Great, so how about changing State?
As we know, a component's state, unlike a component's props, should be able to change during a component's life cycle. Giving a **mapDispatchToProps** as a second argument to connect() allows you to specify which actions your component might want to dispatch. It passes relevant **Action Creators** onto your Component. 

Huh? Action Creator? You mean an Action? 
An Action Creator is a function that returns* an action. It's also called an Action Object Creator Function. An Action Creator is used to generate an Action. An **Action**, however, is just an object with information on what you want to do; it's simply an object with a Type and a Payload. For example, an action would be {type: add Todo, payload: {"Work harder"}} The action is "dispatched" to the Redux store which holds the state for our App, and that is where a **reducer**  handles the action. 

A Reducer? Huh?
The reducer, is just a function with a switch/case statement. i.e. If the type is "add Todo" then do this: "Work Harder". The reducer then passes the action to the Component and returns a new state.

But what if I went to pass a function through an Action Creator, not just an Action/Object?
This is where Redux **thunk** comes in: Thunk is a middleware that looks at every Action that passes through the system, and if it’s a function, it can call that function. Problem solved!


Sometimes it's great to review concepts in layman's terms! I hope this blog helped! 











