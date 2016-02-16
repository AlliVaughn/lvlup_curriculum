*Ready for more?! Ok then! Let's do the thing.*

 
## Setting the Default page 
<!--(http://docs.railsbridge.org/intro-to-rails/setting_the_default_page)-->

### Setting the default page
* First, Let's take a look at what routes we currently have. Type the following into your terminal:
```
rake routes
```
* What we are seeing?
* Head to *https://rails-demo-YOURC9NAME.c9users.io/*. We get an error!  That's because we do not have this page set as any *view* yet. 
* We do have another view though, right?  Do you remember what it's called? Yep!  *Topics!* We were just there. 
* How do we set the main page to be that *topics* view, since we don't have a main page at this point? (...or maybe ever!)
* First, find the following file on the left side of your C9 page:
```
config/routes.rb
``` 
which can be found on the left hand file structure in your C9 window, and double click it to open it.
* Take a look at what you see.  What do you think this page does? 
* Now, add the following at the top of the page, beneath the line ```Rails.application.routes.draw do```: 

```
resources :topics
root 'topics#index'
```
* *notice that rails adds many hints. Scroll down this page and find the word ```end``` at the bottom.*
* *This is important, because it ends the routing file!*
* *Move it up beneath the two lines you just added, and save the file* 
* Now, go revisit your site, but this time at *https://rails-demo-YOURC9NAME.c9users.io/*, without the  "/topics" portion.
* You have just set your main landing page of your site to be the "topics" view. 
* In the future, if decide on a different page to be your main view, you would create another view and tell Rails to route to *that* page instead. 
