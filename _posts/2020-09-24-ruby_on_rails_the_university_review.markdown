---
layout: post
title:      "Ruby on Rails: The University Review"
date:       2020-09-24 19:18:22 +0000
permalink:  ruby_on_rails_the_university_review
---


In the middle of my journey in the Flatiron School, we were asked to create our first Ruby on Rails application. Rails was definitely a learning curve, in that it contains an incredible amount of "magic". We had come from learning Sinatra, which is fairly straightforward. Rails is a lot more powerful, letting you create powerful apps using conventions. However, it wasn't always easy to understand, and definitely took a lot of getting used to.

For my application, I decided to make a University Review website, where a user could read and write reviews about Universities. They can view the entire list of Universities, and even add a university that is not listed. This is my idea of a website that I would have really found useful years ago, during my college admissions process. Who's better to tell you about a school than a current student or alumni? 

One concept that really struck out to me in this project was the concept of ActiveRecord Relations. We were asked to use ActiveRecord Query methods in our model. What this means is that in our  model we would need to ActiveRecord query of some sort, such as "where."

A "where" query for example goes into your database and returns an ActiveRecord::Relation, which is similar to an array, but it's essentially a collection of objects. 

If I use that "where" method in my Review model, to try to find the instance of a Review with the highest rating, I can then access that instance in my Controller and then a View. In that View however, that instance variable is not an instance of a review with the highest_rating; it is an ActiveRecord::Relation collection. It is easily a "promise" to retreive that review, but not the review itself.

Now if I try to access this collection of objects, in the form of a instance variable in my view, I would have to append .last or .first or .find(id) to return a single object.

It really took working through my program over and over again and lots of troubleshooting to realize this concept. Once I did, I was able to easily access objects in my views.
* 
