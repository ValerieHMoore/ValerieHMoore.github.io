---
layout: post
title:      "CLI Data Gem Project: RailTrails"
date:       2018-07-23 14:47:00 +0000
permalink:  cli_data_gem_project_railtrails
---


As I approached my first Flatiron project, I realized I should pick a website I enjoy, since I’d be spending a week with it, scraping data and presenting it to the user in a friendly interface. The successful examples provided by my instructors and the Learn.co platform included “best of” lists such as favorite cake recipes, world’s best restaurants, top 25 video games, etc. Another category of examples were apps where you enter your zip code and receive relevant information, such as movies or meetups near you. Finally, two levels of scraping were required on this project: first the user gets the list, and then they have to be able to choose any item on the list and drill down to the details. For example, they should be able to get the ingredients and the directions for a recipe, or a plot summary and the stars of a movie.
 
I chose to scrape a list of rail trails on Traillink.com. Many abandoned railroad lines have been changed into recreational trails for bicycling, walking, horseback riding, snowmobiling, etc. In my RailTrails app, you enter your zip code and get a list of trails near you. Then you choose one of the trails on the list to see more details: length in miles, state(s) where it’s located, surface (gravel, paved, etc.), endpoints, and a full description of the trail. There were tricky things I couldn’t include in my first project, such as a clickable map showing all the trails.
 
My first hurdle was the blank canvas problem: where do I begin? I carefully watched an example video and put my project into that format, learning as I typed. Of course, it didn’t really apply to my project, so I wiped it out and started over. Then I carefully put my project into the code I wrote for the student scraper lesson on Learn.co, again learning as I typed. That didn’t apply, either! But reproducing these two projects through my fingers and really working with them and handling the file setup helped a lot. Finally, I began to understand how to get my project to work.
 
The final hurdle was the details. Depending on the zip code, anywhere from five to nearly 100 trails might show up. I didn’t want to load all of the details for all of those trails; I thought it was needless and would slow down my program. I only needed to serve up the details on the one trail chosen by the user. Where to put that data: in every single trail object, or into an array, or a hash, or what? A fellow student came to the rescue, explaining that I could add the detail attributes to the trail object and only return those details for the selected trail. It worked! Happy Trails!


