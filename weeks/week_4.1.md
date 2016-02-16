![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Fun with Deployment to Heroku: aka "Grandma Can See This": 
<!--http://docs.railsbridge.org/intro-to-rails/deploying_to_heroku-->
<!--https://devcenter.heroku.com/articles/git-->

*This will allow you (and Grandma!)to view your site "live", at an external web address that you can give out*
First, Prep your project to be compatable in *production*  with Heroku. 
* Head to your Gemfile, and find the following line: 

```
gem 'sqlite3'
```

* Delete that line and replace it with the following code: 
```
group :development, :test do
  gem 'sqlite3'
end

group :production do
  gem 'pg'
  gem 'rails_12factor'
end
```


* Save the file
* In the terminal window, type: 

```
bundle install --without production
```

*Watch Rails install all of your gems and dependencies! Ooooo. Shiny.*

Heroku, your deployment server, works with Git and GitHub to deploy your site.
*First,*In order to use it, you need to add your changes to Git and push to GitHub.

* Let's see where we are currently: 

```
git status
```

*take a look at your changes*

```
git add .
git commit -m "Changed Gemfile for Heroku"
```
```
git push origin master
```

*We need a place to put our production site so that anyone can see it.* 
*We want folks to see what we are doing, right?*

*So, Second*, Let's Create a Heroku Remote like we did for Github, but from the command line.
*From Heroku:* "The *heroku create* command creates a new application on Heroku – along
with a git remote that must be used to receive your application source."
For Instance, type the following command in your terminal: 

```
$ heroku create
```
This command creates the following, but with different words and numbers. 


```
Creating falling-wind-1624... done, stack is cedar-14
http://falling-wind-1624.herokuapp.com/ | https://git.heroku.com/falling-wind-1624.git
Git remote heroku added
```
*If your terminal does not say that your heroku has been added, raise your hand!*

Each Heroku address is unique. 
Why? Think about it and discuss.  
* find your heroku web address in terminal. It should look like this: 

```
https://firstword-secondword-number.herokuapp.com
```
This is the address of your *production* repository on Heroku! 

The following command lets you confirm your Heroku Remote address: 

 ```
 git remote -v
 ```
 
*Next*, Push your Github content to the Heroku repository you've created:  
* Run the following command in terminal: 
 ```
 git push heroku master
 ```
* You should see a bunch of building, an d it will take a minute. 
* You may see some warning messages. Disregard for now. 
* Look for the following message, accompanied by YOUR repository identifiers. 
```
remote: Verifying deploy.... done.
To https://git.heroku.com/sleepy-ravine-7293.git
   664d1a4..ccc0fcc  master -> master
```

*Finally*, we need to create the Database for the live site.
* In terminal, run: 

```
heroku run rake db:migrate
```

* There! You have a remote all set up!
  
Ok!  Open a browser tab, and navigate to your live site URL we created above, 
which resembles the following: 

```
https://firstword-secondword-number.herokuapp.com
```

* *admire your shiny new live site!* 
* Hmmm...
* [Chloe is unimpressed, but stay tuned!](https://s-media-cache-ak0.pinimg.com/736x/28/ef/20/28ef204478b114e7fb81d2bfe77444ac.jpg)
* Let's head on back to the development site and see what we can do!


#The Site is OK, but What Can We *DO* With It and how can we 
make it look better? 
I'm with Chloe: Let's get to work. 
First, we will deal with functionality and then we will make it look interesting.