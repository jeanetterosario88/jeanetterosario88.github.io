---
layout: post
title:      "Redux Thunk and API Calls"
date:       2021-01-22 16:16:31 +0000
permalink:  redux_thunk_and_api_calls
---

In general, Redux store doesn't know anything about asynchronous logic. By default, Redux actions are dispatch synchronosuly.  It only knows how to synchronously dispatch actions and update the state. Luckily, Redux has a middleware called Thunk". To use it, we install the redux-thunk  npm package.


Thunk lets us write functions that get dispatch and getState as arguments. The thunk functions can handle async logic; they can read the state and dispatch actions. Specifically, we can dispatch an action once an asynchronous operation is completed.

For example, we can make an AJAX call to an API endpoint to request information. Let's say for example, we make a Get request to get cat pictures from /examplesite/catpictures. We can then dispatch an action containing these images. We can then update the state in our reducer. 

We would update state by adding a case to the reducer to load these pictures, or data, onto the store. We replace any existiing cat picture data with the current data. We return the current action.payload so that that is our new state.
