---
layout: post
title:      "Sandwich Platter"
date:       2018-09-06 15:13:44 -0400
permalink:  sandwich_platter
---


My second Flatiron School project was to build a very basic web app; I called it Sandwich Platter. Users can sign up or login to see sandwich recipes. In keeping with the ActiveRecord CRUD (Create, Read, Update, Delete) project requirements, you can only Create, Update or Delete your own sandwiches; you can Read all of the sandwich recipes.

I started by downloading a pdf of 200 sandwiches from Wikipedia for seed data. This data included the name of the sandwich, a thumbnail photo, country of origin, and ingredients/directions. I only wanted the name and the ingredients, so I converted the pdf to Word and then to a csv file to strip out all the images. I then imported to Excel and cleaned up the data by deleting the country column and making sure each sandwich had only one row. A number of the sandwich names had special characters from other languages, and I was afraid those would mess up my code, so I manually changed them to unaccented English letters. I edited the sandwich ingredients/directions for clarity and brevity, and removed some recipes. Finally, I had a list of about 175 recipes for my seed data. These sandwiches appear on the app’s list of All Sandwiches, but users cannot Update or Delete them.

In testing my web app, I mistakenly created a duplicate user that was causing errors. I had to drop into a Tux session to fix that. According to the description at RubyGems.org, “Tux dresses up Sinatra in a shell. Use it to interact with your helpers, view rendering and your app’s response objects. Tux also gives you commands to view your app’s routes and settings.” I didn’t want to create temporary application controller routes and erb views for a one-time purpose. With the help of another student, I was able to delete User 2 and User 3 in my terminal. While I was at it, I deleted some blank sandwich recipes that were created during the seed data import process. I was able to finish testing all my routes and make sure that users can only Update and Delete their own recipes.

Bon Appetit!

