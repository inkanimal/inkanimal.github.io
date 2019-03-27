---
layout: post
title:      "Going off the rails..."
date:       2019-03-26 23:15:35 -0400
permalink:  going_off_the_rails
---


##3 For my rails project I built a simple fitness tracker. One can record the exercise they did, including how many sets, reps and the weight they used. They can also search through a list of preinstalled exercises for insperation. All their workouts are recorded by date so they can easily look them up at a later date. 

One of the more challenging parts to this project was integrating the facebook sign-in option. It is mostly annoying on facebooks' end of things. 

Instead of using the dotenv gem, I decided to use the credentials.yml file built into rails  5.2. This is actually pretty easy to use, once you get your app_id and app_secret from facebook. 

Once you have those you can store them in the credentials.yml file. You need to use the terminal to access it. 

In the terminal you put  `EDITOR="atom " rails credentials:edit` You may need to add "--wait" following the name of the text editor you are using, in my case, atom. This will open the credentials file where you can place your facebook secrets.

 ```
 facebook: 
         APP_ID: 123
	     APP_SECRET: abc
	```
	 
	 
Since I used devise, I put the APP_ID and APP_SECRET in `initializers/devise.rb` like this:

```
APP_ID = Rails.application.credentials.facebook[:APP_ID]
APP_SECRET = Rails.application.credentials.facebook[:APP_SECRET]
config.omniauth :facebook, APP_ID, APP_SECRET
```


	 
The rest is just pretty staight forward omniauth stuff using the devise gem. You can find their documentation here:
https://github.com/plataformatec/devise/wiki/OmniAuth:-Overview
				 
For me the challenging part was facebook and their never ending changes to their menus and layouts. Perhaps is is just my loathe for their ads manager interface, but that is a story for another day. Happy coding.

				
	
