---
layout: post
title:      "Devil is in the details"
date:       2018-10-08 18:19:09 +0000
permalink:  devil_is_in_the_details
---


I recently finsihed my Sinatra project. It was a project I found pretty challenging. Mostly because of the way I went about building it. Too much, too soon. I built a simple fantasy basebeall app. In it, you could create a team, draft player and pick or create a stadium. Nothing earth shattering complex, but the way I went about it made it extremely difficult. There are two things I am taking away from the this project; 1. details are everything. 2. Trying to build too much at once is a recipe for disaster. 

Both of these things go hand in hand. I had my entire project basically working except for one of the routes. No matter what I did I could not clear the errors. I finally went over every part of my code where the problem was occuring line by line and character by character. I eventually found the problem. I was missing an underscore in one of my lines of code. This: player_<%=player.id%> is a lot different than this: player<%=player.id%>. That one underscore changed everything. 

This brings me to the second part. If I had not build out so much of my project it would have been easier to spot the problem. Going part by part and testing each part as you go is the simplest way to build. I have a tendency to get ahead of myself and therefore run myself into extra and uneeded time and work. It is something that I am working on and hopefully the lessons I learned in this project will make my life going forward a lot easier. 

Go slow. Double check your work. Be good to people...
