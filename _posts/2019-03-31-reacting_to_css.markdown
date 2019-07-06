---
layout: post
title:      "Reacting to CSS"
date:       2019-03-31 22:47:54 -0400
permalink:  reacting_to_css
---


CSS styling always seemed messy and cumbersome to me, and I mostly managed to avoid it with two simple tricks: changing the default font-family and using eye-catching [background images](http://valeriehmoore.com/the_big_picture_on_my_rails_project). But for my final project, I wanted something better.

Styled-Components is a clean and simple way to put CSS into a React app. To install, type the following in your terminal:
`npm install --save styled-components`

In your components folder, create a file with a descriptive name for your design element. For my background image and global font formatting, I put the following in Wrapper.js; note the backticks around the CSS below:

![](https://i.imgur.com/GndnTFr.png)

To use this style, I imported the Wrapper component into App.js and wrapped my code in it as follows:

![](https://i.imgur.com/fgj9lO5.png)

I added styled-components for Header and Button, and used them as follows:
```
<Header>Grocery List</Header>
    <Link to="/items/new/item"><Button type="button">Add Item</Button></Link>
```

I created a styling folder and dragged in all my new styled-components and the background photo. Now all my CSS is in one place, with sensical names:

![](https://i.imgur.com/A9zp6eu.png)

In Visual Studio Code, I installed an extension called [vscode-styled-components](https://github.com/styled-components/vscode-styled-components) for syntax highlighting that makes the CSS much easier to read.

Styled-Components has many other features and capabilities for styling your React app; find them [here](https://www.styled-components.com/).


