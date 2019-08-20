---
layout: post
title:      "WordCamp Lehigh Valley 2019: Part 1"
date:       2019-08-20 17:44:47 +0000
permalink:  wordcamp_lehigh_valley_2019_part_1
---


I attended my first WordPress conference a few days ago in Bethlehem, PA. My key takeaways from the presentations I attended are divided into two blog posts; this is part 1.

## From Zero to Hero: Create a Site in 30 Minutes
By [James E. Taylor II](https://jetsquared.com/James) of [JetSquared](https://jetsquared.com)

Soon I’ll be building a portfolio site, so this is the presentation I was most interested in. James covered the following step-by-step:
* Get a server with control panel; he recommended (but receives no compensation from) Digital Ocean and CyberPanel. On Digital Ocean, choose a server that is geographically close to you. For a portfolio site, a $5 dollar-a-month plan is fine.
* In CyberPanel, the first thing you should do is login and change your password.
* Point a domain to the server and enable SSL. 
* Install WordPress for the domain; this will vary depending on your hardware and software setup. James used a LAMP stack (Linux, Apache, MySQL, PHP).
* Build your new WordPress site; James used a free library called coblocks.

James also gave me additional help afterwards regarding how to migrate my existing Flatiron School blog domain in the above setup. Flatiron purchases the domain for you for one year when you’re a student, and then you can purchase it from Namecheap for $12.98 for one year – amazing! 

## What Does Your Brand Look Like in a Voice-First World?
By [Chip Edwards](https://createmyvoice.com/)

This was the most futuristic presentation of the day, starting off with statistics I wasn’t aware of: 30% of Americans own smart speakers, and 20% of all internet searching is now done by voice. The growth in this area is exponential; people are moving away from laptops, and moving towards other devices they can talk to instead of type on. This brings up the fascinating question, “What is our brand when people aren’t seeing it?” Companies need an “earcon” rather than an icon. Chip showed a slide of familiar company logos, and then played their signature sound and had us guess which company; very few sounds were familiar. One company had a number of different versions of their earcon, in different musical styles for varied applications.

When coding for your website, you should use [Speech Synthesis Markup Language (SSML)](https://developer.amazon.com/docs/custom-skills/speech-synthesis-markup-language-ssml-reference.html) to optimize the way your text sounds when spoken by the smart speaker. For example, you can specify different voices for different sections by [name](https://developer.amazon.com/docs/custom-skills/speech-synthesis-markup-language-ssml-reference.html#voice). Chip showed us that in addition to SSML tags, you can also get better audio results by adjusting standard HTML and CSS. For example, audio devices read headers and subheads better when they are coded using different size ```<h>``` tags ```<h1>, <h2>``` instead of font size numbers ```<p style="font-size:30px">```.

Try to make your domain name unique from an aural perspective. The following domains will all sound the same on Alexa: 2cents.com, twocents.com, tosense.com, and tooscents.com. You can use [rhymezone.com](https://www.rhymezone.com/) to see which words sound like names you are considering.

Chip will be presenting at [WordCamp NYC 2019](https://2019.nyc.wordcamp.org/speaker/chip-edwards/), and an earlier version of his presentation is available [here](https://wordpress.tv/2019/06/26/chip-edwards-what-does-your-brand-look-like-in-a-voice-first-world/).

Stay tuned for Part 2!


