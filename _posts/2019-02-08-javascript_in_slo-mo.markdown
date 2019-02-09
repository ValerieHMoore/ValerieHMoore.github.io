---
layout: post
title:      "JavaScript in Slo-Mo"
date:       2019-02-08 21:56:38 -0500
permalink:  javascript_in_slo-mo
---


[Separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) and the need for incremental testing makes JavaScript coding a slow-motion operation. In my previous Ruby on Rails project, I wrote discrete pieces of code in models, views and controllers. This time, I added a JavaScript front end to that app by refactoring a lot of functionality into one file.

Sandwich Platter is a recipe app with sandwiches as the topic. Instead of redirecting users to separate pages, my app now displays all the information at one url. It looks like one-stop shopping, until you examine the code.

I created a new landing page where the [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) content would be sent. Then I started building the JavaScript file in tiny increments. Once users log in, they see a page with three links: All Sandwiches, My Sandwiches, and Build a New Sandwich. My first function does only one thing: listen for a click on the All Sandwiches link. You can see that I put in a message to the console to test this before moving on:

```JavaScript
function listenForClickAllSandwiches() {
    let doc = document.getElementById('all-sandwiches')
    doc.addEventListener('click', function (event) {
        event.preventDefault()
        console.log("My button works");
        getAllSandwiches()
    })
}
```

Once I saw the “My button works” message in the browser’s console, I wrote the next step. This time, I displayed the sandwich index data in the console to confirm:

```JavaScript
function getAllSandwiches() {
    $.get("/sandwiches.json", function(data){
        let sandwiches = data
        let emptystring = ""
        sandwiches.forEach((sandwich) => {
            emptystring += '<li>' + sandwich["sandwich_name"] + '</li>';
        });
        console.log(data)
        $("#ajax-content").html(emptystring)
    })
}
```

The browser showed these two confirmations as follows:

![](https://i.imgur.com/tXjVKwa.jpg)

I wrote similar code for My Sandwiches: listenForClickMySandwiches() and getMySandwiches(url), with the same type of tests.

For users to build a new recipe, I had to write four functions: listenForClickCreateSandwich(), getBlankSandwichForm(url), listenForClickSubmitSandwich(), and postSandwichData(url, data) to create the new sandwich instance in the database. I commented out the previous console.log message each time and sent a new one with the name or the data for the next function.

There were many other components to this project, but the moral of the story is: write a little bit of code and confirm that it works before moving on.
