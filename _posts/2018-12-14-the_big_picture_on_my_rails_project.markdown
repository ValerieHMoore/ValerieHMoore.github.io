---
layout: post
title:      "The Big Picture on My Rails Project"
date:       2018-12-15 02:32:29 +0000
permalink:  the_big_picture_on_my_rails_project
---


Rails ActiveRecord associations link two models together via a join table so we can program interactions between them with a minimum amount of code. The official RailsGuides image (shown below) that explains `has_many :through` associations has three boxes: physicians, patients, and appointments. The Appointment model is the join table; it belongs_to :physician and belongs_to :patient. Join tables contain the ids of the tables they are joining, which are physician_id and patient_id in this example. Join tables may also have fields of their own, in this case appointment_date.

![](https://i.imgur.com/tRpudhv.png)

A problem I encountered in setting up my Rails project is that this diagram is missing something: the app’s user. Our project specs require “standard user authentication, including signup, login, logout and passwords.”

## The Big Picture: App Diagram

Here is my app diagram:

![](https://i.imgur.com/ssDMJGj.png)


My app is called Rails Project Sandwich Platter, which is a sandwich recipe app. Here you can see that a user has_many sandwiches and a sandwich belongs_to a user. The Sandwich and Filling models are linked via the join table Sandwich_Filling, shown in orange. The Sandwich model has_many :fillings, `through: :sandwich_fillings` and the Filling model has_many :sandwiches, `through: :sandwich_fillings`. This makes it possible for a user to build instances of the filllings while building a sandwich, and/or to build a filling and then add it to a sandwich.

In my app, users create an account and then they can see all the sandwich recipes from all the users. They can create, edit and delete recipes they have created, but they will receive error messages if they attempt to impersonate another user.

When a user creates a sandwich, they can check a box to indicate if a sandwich is grilled and/or open-face. This is a boolean which normally displays as true or false, but I have a user-friendly method that displays yes or no instead. Users can click on All Sandwiches, Grilled Sandwiches, Open-Faced Sandwiches, or My Sandwiches to see different views of the data. 

## The Big Picture: Background Images

I wanted to use edge-to-edge background images on the different views in my app, and searched the web to learn how to do that. I found mouthwatering, free sandwich photos on Unsplash.com: a grilled sandwich for my grilled sandwiches page, an open-face sandwich for my open-faced sandwiches page, etc.

I renamed the photos for my own convenience and dragged them into the assets/images folder in my app. Then in the stylesheets/application.css file, I created a body class for each one as follows, using the CSS property `background-size: cover;` (saddlebrown is the font color in the example below):

```
.sandwiches-index{
    color: saddlebrown;
    background-image: url("sandwich-index.jpg");
    background-size: cover;
}
```

Finally, I called that class on the desired view:

```
<body class=sandwiches-index>
<!--rest of code here-->
</body>
```

`Background-size: cover;` was very easy to implement and makes my app look delicious!

