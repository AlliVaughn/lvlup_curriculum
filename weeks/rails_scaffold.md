# What Makes Rails and Scaffolding so *AWESOME*? ( Hint:  It's not Cats.)

Recall that in C9, You Choose "Ruby" as a project type, right? This AUTOMATICALLY generates a Rails instance!  (In a local desktop IDE, You would use the rails command to create the basic skeleton of the application.) 

## By *HAND*, you can: 
* Create Rails Active Records (Models), because they are the business objects you'll be working with in your controllers.
* Generate Migrations that simplify the creating and maintaining of database tables and columns.
* Write Controller Code to put life in your application.
* Create Views to present your data through User Interface.
* Further Migrate that database as other models are created!  

## Rails Does Most of this tedious work *FOR* you! 

When we initiate a scaffold by enetering the following on the terminal command line:  
```
rails generate scaffold topic title: string, description: text 
```
Rails knows that we actually want it to create a model file, controller file, CRUD code,  view files,  stylesheet and js files for topic, and it automatically creates those files with starter code! ( A scaffold is a cool tool, actually, as it *hints* at how to do something, and is pretty great for learning! )

By running the next command in our terminal:
```
rake db:migrate
```
Rails also knows to hook all of this to the database, SQLite! Voila! 

Pretty cool!  

When we run our project and go to the /topics window, we see a bunch of usable stuff, already up and running!  

As you get more familiar with teh  conventions of rails, CRUD, M-V-C etc, it will be easy to create your own files from simply ``` rails generate ``` rather than the scaffolding, and you can read up on the syntax for that at: 
## [Rails Guides](http://guides.rubyonrails.org/): The mother ship for Rails! 




