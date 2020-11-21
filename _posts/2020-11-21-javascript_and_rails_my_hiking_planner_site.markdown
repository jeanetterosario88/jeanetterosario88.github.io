---
layout: post
title:      "Javascript & Rails: My Hiking Planner Site"
date:       2020-11-21 23:43:56 +0000
permalink:  javascript_and_rails_my_hiking_planner_site
---

For our fourth Flatiron School project, we were asked to create a single page application utilizing Javascript, HTML, CSS as our frontend tools and Ruby on Rails as our backend and API. I decided to create a Hiking planner, where anyone can add and view Hiking Itenaries; sorted by number of likes, and categorized by city. You can even add a city if you don't see one listed.

So how does this satify my project requirement? Well I wanted to store all that hiking data in my backend and have it easily accessed by someone using the site, therefore creating an API.

An API, or Application Programming Interface is essentially a way for a system to communicate with other systems in a way that allows for easy interactation. There are a lot of public APIs available where you can see easily access data to then add into your own project. But Ruby itself can serve as an API if you have data that you'd like to share; you can create the API from scratch.

So how do we access and share this data? Well for one, we convert our data into JSON. JavaScript Object Notation is a data-interchange format that is very easy for people and computers to read and share. It is lightweight, and it works very well with Javascript, of course. But it is also easy to use with Ruby, Python, JS and more. This is because this object notiation is text only; it converts all your data into strings, " ", and stores them in easy-to-read key-value pairs such {"books:" "Catcher In The Rye"}. 

So how does JSON work? Well it's "serializes" your objects. Serialization can convert complex objects into byte strings that can be easily sent through wire to anywhere. After the byte strings are transmitted, the receiver will have to recover the original object from the byte string. This is known as "deserialization."

For my project, with Ruby on Rails being my backend, all I had to do to convert my data to JSON was install a  gem called "'fast_jsonapi' which allows you to generate Serailizer classes for your object. There you can customize what data inside your object you'd like to share, and therefore, "serialize". 

After that, if your frontend, in my case, Javascript, wants to access this backend API data, it can get  "fetch" that data from one of your routes, such as https://.../books/2, for the second book listed, like "Catcher In the Rye". This would be known as a Show route with the method "Get", to get the data.  You'd specify that route in your config/routes folder in your Rails backend. After that, you'd tell your frontend, in this case, Javascript, to convert that data into JSON information, and there you have it. Now your frontend can also actually use this data since Javascript can easily read JSON. 
