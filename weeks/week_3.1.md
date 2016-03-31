![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Intro to Rails: Create a Migration & CRUD w/Scaffolding  

* Open your terminal and type the following: 
```
rails generate scaffold topic title:string description:text
```
*Hrm. "Scaffold"? I mean, [DaVinci](http://faculty.virginia.edu/Fiorani/NEH-Institute/essays/yerkes) used those, right? Why are there scaffolds in Rails though? * 
 
* *Scaffold* creates more files automagically in order to *support* your development! (Pause: talk about what's created and what they're for)
* [About Framework Architecture](http://docs.railsbridge.org/intro-to-rails/rails_architecture)
* Now, we need to *migrate* the Database so that it can accept new entries!  
```
rake db:migrate
```

* "Rake?" Are we clearing leaves?  
Well, no.  *Rake* (or "R(uby m)ake") is a command line tool that allows you to run small Ruby programs (tasks) that you use often in your application.
Neat! That helps!  It would take quite a while to script that by hand! 

## [Why is it so Cool!?](rails_scaffold.md) 

## CRUD with Scaffolding:
<!--(http://docs.railsbridge.org/intro-to-rails/CRUD_with_scaffolding) -->

## All About CRUD:

At the core, most database driven web sites are the same.
They need to store records and provide a way to do the following:
* *C* reate new records in the database
* *R* ead  or show the records in the database
* *U* pdate those records
* *D* estroy/*D* elete those records wen we don't need them anymore

*[A bit of Light Reading, if you're interested:](https://s-media-cache-ak0.pinimg.com/originals/c8/76/4a/c8764a5c78d5bd752ec626a97421b5d0.gif)

[CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)

## Now that we have that square, let's get CRUD-dy: 
* If your app is not running, click on "Run Project" button at the top right of your C9 menu bar
* Click on the url prompt for your project, which should resemble this (https://rails-demo-YOURNAME.c9users.io) and add "/topics"
* Hit return... *Wow! Stuff!*  YOU made that happen.   
* Go ahead and play with the functionality of the page for a bit, and we will discuss what you are seeing and why it is here. 
* You will notice that there is not really any terrific styling yet. 
* [DON'T PANIC!](https://d3vjvsn2tynjug.cloudfront.net/v2/w_450,h_450/https%3A%2F%2Fs3.amazonaws.com%2Ftanga-images%2F3xprykg2quwd.png)
* Right now, we are concerned with what the app is *Doing*, not what it looks like. 

[OVERVIEW](overview.md)
