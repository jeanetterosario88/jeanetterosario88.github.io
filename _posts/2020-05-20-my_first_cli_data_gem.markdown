---
layout: post
title:      "My First CLI Data Gem & Scraping a Table"
date:       2020-05-20 15:28:23 -0400
permalink:  my_first_cli_data_gem
---


About six weeks into my Flatiron experience, my cohort was asked to create our very own CLI project! The task felt intimidating, as it was our first independent project, where we'd have to use all that we've learn about Ruby thus far. We were asked to scrape data from a webpage and create a CLI to provide access to data from said web page. We were asked to have the data goes one "level" deep, where a user could make a choice and get information from that choice.

For my project, I decided to scrape data from one of my favorite websites, www.broadwayforbrokepeople.com . It is a simple website that lists all current and upcoming Broadway shows and gives you information. Most people use the site to look up the shows' cheap ticket policies. Most Broadway theaters in the city actually sell discount tickets! 

Luckily, I had experience scraping and creating a CLI from our previous lessons. The most difficult part of the project was scraping the data off the broadwayforbrokepeople.com page. The page itself looks very simple, but it's also mostly one large table. I had had no experience scraping data off a table. The trick was to find the table, and within that table, search for each row, and within each row, search for the column. This is how I was able to access specific boxes within a table. It also took a bit of work to clean up the text. There were empty hashes, awkward hashes, and so it was a task to write code that cleaned up the information. 

After that, the path was a bit more straight-forward. In the end I got my CLI to work! It's a CLI that I would personally use, so I consider this project to have been very fun to write!

https://github.com/jeanetterosario88/brdwy4brkppl.git

