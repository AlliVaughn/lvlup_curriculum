## Introduction to Full Stack Development: Or, Reasoning Saves the World
<!--(http://docs.railsbridge.org/intro-to-rails)--> 

## Sign Up for All the Things!   
### Visit the following links and sign up for each service. 
* For our course, please use the same credentials for each service. It makes it easier.*
* [Sign up for a Cloud9 IDE account](https://c9.io) 
* [Sign up for a Github account](https://github.com)
* [Sign up for a Heroku account](https://heroku.com)



## Overview: Setting the Stage: Environment and  Expectations
### The State of Things 
 <!--(Most Tech employees are currently white and male 20-45 y/o, Women & Minorities in Tech much lower,-->
 <!--Workforce Projected to grow significantly by W/Minorities in next 10, BUT number of W/M expected to -->
 <!--enter Tech DECREASING.  Houston: AUSTIN, we have a problem. ) -->
 #### We WANT YOU! 
 ( Supporting readings from White house directive on STEM and NSF/ Other supporting stuff)  
 [Census Report on STEM Rep Women/Minorities 2013](https://www.census.gov/prod/2013pubs/acs-24.pdf)
 [Nat. Ctr for Women in Technology Statistics](https://www.ncwit.org/blog/did-you-know-demographics-technical-women)
 [Fed. B. of Labor Stats](http://www.bls.gov/cps/cpsaat11.htm)
 [clear diagram of teh projected increase in minorities in workforce by 2022](http://www.bls.gov/opub/mlr/2013/article/labor-force-projections-to-2022-the-labor-force-participation-rate-continues-to-fall.htm)
 
 ### What can we do about it?  
 Why YOU, yes you, should learn to program. 
 [Douglas Rushkoff](http://www.rushkoff.com/about/)
 [Treehouse blog Article about Practical application for non-programmers](http://blog.teamtreehouse.com/havent-started-programming-yet) 
 
* Show and tell of MY Local IDE, The Lvl\U/p IDE, Demo site 
* Q & A
* The Great Duck Migration

### Meta-Goals:
When you have completed Lvl\U/p, you should understand:

* Vocabulary (Discussion of activity each week, Sign up for Evernote)  
* Some basic programming language syntax and command line syntax (Ruby)
* How to try out code in a test console (Ruby code in IRB)
* How to go from requirements to a new working application in a framework (Rails)
* How to get your application online (Heroku) 
* The basic tools that a developer uses (source control, editor, console, cloud local development server)
* A bit about the  state of the demographics of Technology presently, Projections for the next 10 yrs, and
 next steps you can take. 

### Tools of the Trade
 
* Rubber Duck, Various Games, Sandwiches, IoT, EACH OTHER(Community) 
* Cloud 9 Internet Development Environment (C9 IDE)
* C9 IDE includes the following: Ruby, Rails, Bundler, SQLite, a text editor, Terminal, and more! 
* Git and Github
* Heroku
* Bootstrap
* HTML/CSS


## C9 Workspace
<!--(http://docs.railsbridge.org/intro-to-rails/getting_started)-->

### Begin by setting up a new Workspace in C9 IDE: 
* Login to C9
* Create a new workspace 
* Name your *Workspace* for the app we will create ("your_new_workspace_name")
* Add a description.
* Select the "Ruby" icon to indicate we are using a Ruby IDE. (Note the others! Nifty, eh? ) 
* Click the create workspace button 
* Creating a workspace automagically generates a "Rails New" instance, and names it "your_new_workspace_name" anyway, so no need for that command!

### Environment and Framework Petting Zoo
 
* open a terminal (if not already open)
 Activity: [Ask Ubuntu](http://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)
* type "ls" to list the contents
* compare to the files you see on the left
* run the project by clicking the "run" button (which is like running "rails s" in a traditional local development environment) 
* click on the url in the terminal window and see your page holder for your app!  


## Fundamentals of Coding:
 Intro discussion about how many languages there are(Solicit names of languages and discuss the history a bit.) 
 [O'Reilly Poster](http://cdn.oreillystatic.com/news/graphics/prog_lang_poster.pdf)
###  Pseudocode
* Activity: Write steps to make a pb & j sandwich. 
* Watch this [Video of CS50 Pseudocode](https://www.youtube.com/watch?v=KUB-aJXquUA)
<!--17:08-25:25-->

[Pseudo code Intro: CS 50: Harvard OCW](https://www.youtube.com/watch?v=UuFWYOnHwGM)

<!--b.  PB & J: pseudo code Handout:  http://static.zerorobotics.mit.edu/docs/team-activities/ProgrammingPeanutButterAndJelly.pdf-->

<!--c.  Railsbridge Intro to Ruby: Go through this: http://docs.railsbridge.org/intro-to-rails/ruby_language-->

* Discuss. 

### A Whole New World (of Programming)
<!--(http://docs.railsbridge.org/intro-to-rails/ruby_language)-->
 
* Activity: Patterns in Language ( Simple Article in Chinese, Japanese Hiragana or Arabic) 
* Basic programming syntax in Ruby
* Practicing simple calculations, variables, arrays, loops and conditionals
* Introduction to the console (IRB) to try out code
 


## Add The Project To A Git Repo
This cloud environment is nifty, but, um, how do we *keep* our stuff?  Where will it live? 
Imagine your project is a cold puppy outdoors in the Winter... That's sad, right? 
Let's help our furry friend. 

* Activity:  Jenga 
* We will use this resource: [Push your C9 Project to GitHub](http://lepidllama.net/blog/how-to-push-an-existing-cloud9-project-to-github/)
* Open gitHub and Sign in, and place the tab next to your C9 dashboard tab
* In C9 dashboard, click "settings" (the gear) button on the right. 
* In the menu to the left click on "connected services". 
* click "activate" next to gitHub and follow instructions to connect **OR** If you've already connected gitHub, you can skip this step. 
* Click “ SSH key” and copy the value which appears.
* Go to your open gitHub tab and click on your picture in the right hand corner and open your profile.
* click on the  "edit profile" button on the upper right. 
* look at the left hand menu and open "SSH keys" 
* click the  "Add SSH Key" button the upper left Label the field C9, and paste in your key that you copied from C9.
* click "Add Key"
* [create a new repository for your project](https://github.com/new) (or click the plus sign from your gitHub dashboard) 
* *Repository name: use the same name as your C9 workspace*
* *Description: Add a description*
* *Leave the repo as "public" and don't check the  "Initialize this repository with a README" button.*
* click "create repository"
* Now copy the SSH link. By default GitHub shows the HTTPS link, you will need to toggle it to SSH first! It will look something like:```git@github.com:yourname/yourrepository.git```
* Open your C9 project window, and go to the terminal. Set your git config username:```git config --global user.name "Your Git Name Here"```
* Next, also in the terminal, Set your git config email (which should match your github account email):```git config --global user.email "your_email@example.com"```
* Now, Make your current directory a git repository by typing: ```git init```
* Using the SSH link you copied from your gitHub repository, add the remote repository as the origin:```git remote add origin git@github.com:yourname/yourrepository.git```
* Add your files and commits, as you normally would:```git add .``` and then ```git commit -m "First commit"```
* Push your changes:```git push -u origin master```
* Go look at your gitHub repo and refresh:  MAGICAL!  You now have a full copy of all of your work from C9 on a gitHub repo! 
* [Simple Daily Git Workflow: An Excellent Resource!](http://image.slidesharecdn.com/dcnyc10-gitingear-120510030924-phpapp02/95/git-in-gear-how-to-track-changes-travel-back-in-time-and-code-nicely-with-others-30-638.jpg?cb=1397421717)

*Phew! That was a lot! Well Done, You! Let's get back to our project!* 

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


*Ready for more?! Ok then! Let's do the thing.*

 
## Setting the Default page & Deploy to Heroku 
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
## Voting on Topics and Hooking Up Votes and Topics
### Voting on Topics
<!--(http://docs.railsbridge.org/intro-to-rails/voting_on_topics)-->

* Let's create another model, this time for *Votes* on our topics! 
* In terminal:  
```
rails generate model vote topic_id:integer
rake db:migrate
```
* This one is *not* a full scaffold this time. Why not? (Hint, What are we voting on?) 
* *We aren't going to do the full CRUD for votes; they're just going to be*
*considered part of topics as-is.*

### Hooking up Votes and Topics
<!--(http://docs.railsbridge.org/intro-to-rails/hooking_up_votes_and_topics)-->

* First: Tell the Topic model about Votes! It doesn't know they exist yet! 
* Navigate in your  C9 editor to ```app/models/topic.rb ```
* Add the following and save the file: 
```
class Topic < ActiveRecord::Base
  has_many :votes, dependent: :destroy
end
```
* Now, tell the Vote model about Topics! It doesn't know either! 
* Navigate to ```app/models/vote.rb```
* Add the following, and save the file: 
 
```
class Vote < ActiveRecord::Base
  belongs_to :topic
end
```

* What you just changed in Active Record is how the App knows to associate Topics and Votes. Nifty, eh? 
* Finally, let's take a look at how these work in the console! 
* At terminal, type ```rails c```
* Continue with exercise from [Railsbridge](http://docs.railsbridge.org/intro-to-rails/hooking_up_votes_and_topics)

 ## Allow People To Vote 
<!--(http://docs.railsbridge.org/intro-to-rails/allow_people_to_vote)-->

* Add a new controller action for voting 
* Open the following file ```app/controllers/topics_controller.rb```, and add: 
```
def upvote
  @topic = Topic.find(params[:id])
  @topic.votes.create
  redirect_to(topics_path)
end
```
* Now, add a *route* for voting!  
* Open ```config/routes.rb``` 
* Replace ```resources :topics``` with the following: 
```
resources :topics do
  member do
    post 'upvote'
  end
end
```
* Verify that the route has been added by either typing ```rake routes``` in your terminal.
* Now, let's add a voting button to that topics *view* so that we can click on it and vote! 
* Open ```app/views/topics/index.html.erb``` and edit to make sure it matches this: 
```
<% @topics.each do |topic| %>
  <tr>
    <td><%= topic.title %></td>
    <td><%= topic.description %></td>
    <td><%= pluralize(topic.votes.count, "vote") %></td>
    <td><%= button_to '+1', upvote_topic_path(topic), method: :post %></td>
    <td><%= link_to 'Show', topic %></td>
    <td><%= link_to 'Edit', edit_topic_path(topic) %></td>
    <td><%= link_to 'Destroy', topic, method: :delete, data: { confirm: 'Are you sure?' } %></td>
  </tr>
<% end %>
```
* Confirm that your changes have worked by heading back to /topics

### Push your changes to gitHub and then Heroku, as we did previously. 

## Tweaking Things for User Convenience:

## Redirect to Topic List & Creating a New Topic
<!--(http://docs.railsbridge.org/intro-to-rails/redirect_to_the_topics_list_after_creating_a_new_topic)-->

When a user creates a new topic, or edits an existing topic, they are currently shown a page with just that topic.
For our voting app it makes more sense that they would be taken back to the topic list.
In this step we'll change the flow of our app so that the user is taken back to the topics list after they add a 
new topic (create) or edit an existing topic (update).

### Change the topics controller
* Open ```app/controllers/topics_controller.rb``` and look at the create method, and then find this line:
```
format.html { redirect_to @topic, notice: 'Topic was successfully created.' }
```
and change @topic to topics_path like this:
```
format.html { redirect_to topics_path, notice: 'Topic was successfully created.' }
```
The file should now look like the following:
```
def create
  @topic = Topic.new(topic_params)

  respond_to do |format|
    if @topic.save
      format.html { redirect_to topics_path, notice: 'Topic was successfully created.' }
      format.json { render :show, status: :created, location: @topic }
    else
      format.html { render :new }
      format.json { render json: @topic.errors, status: :unprocessable_entity }
    end
  end
end
```
* In the same file, find: 
```
format.html { redirect_to @topic, notice: 'Topic was successfully updated.' }
```
and change @topic to topics_path like before:

```
format.html { redirect_to topics_path, notice: 'Topic was successfully updated.' }
```
### Change the topics *index* view
* Open ```app/views/topics/index.html.erb```and add the following line:
```
<p id="notice"><%= notice %></p>
```

*Adding this line will ensure that the notice message we included in the TopicsController will*
*show up in your index view. You can add this line wherever you want the messages to show up on* 
*the page. Experiment with adding it in different places in your index view.*

* Confirm the Change by navigating to your home view
* Voila! 

<!--Explanation-->
<!--format.html { redirect_to topics_path, notice: 'Topic was successfully created.' }:-->
<!--format.html means that the server should send HTML back to the browser-->
<!--redirect_to topics_path means show the topics list page when we're done creating or updating a topic-->
<!--notice: 'Topic was successfully created/updated.' puts the message into the flash so it will be displayed on the topics list-->

### Push your changes to gitHub and then Heroku, as we did previously. 


## Make The Topic Title A Link & Clean Up Links On The Topics List
### Make The Topic Title A Link
<!--(http://docs.railsbridge.org/intro-to-rails/make_the_topic_title_a_link)-->

Let's go ahead and dispense with the awkward by making the title a link and when it's clicked, show the description.
* Let's start by removing the description. Open app/views/topics/index.html.erb and delete the line that looks like this:
```
<td><%= topic.description %></td>
```
* Also delete the line that looks like this:
```
<th>Description</th>
```
*If you save and try to load it in the browser you should see that the description no longer appears.*

* Now make the title a link by editing 
```
app/views/topics/index.html.erb
```
(again) and replacing this line:
```
<td><%= topic.title %></td>
```
with this:  
```
<td><%= link_to topic.title, topic %></td>
```
* Confirm your changes! 

<!--Explanation-->
<!--<td><%= topic.description %></td>-->
<!--This line was getting the description using .description and just printing it out.-->

<!--<th>Description</th>-->
<!--<th> stands for table header and everything between <th> and </th> was being printed-->
<!--as a table header (bold). We removed it since we removed the description and it would -->
<!--look funny to have the header and the wrong thing below it.-->

### Push your changes to Github and then Heroku, as we did previously. 
## Clean Up Links On The Topics List
<!--(http://docs.railsbridge.org/intro-to-rails/clean_up_links_on_the_topics_list)-->

* Our page is cluttered with some unnecessary links!
* Let's clean those up by removing the "show" and "edit" links and changing "destroy" to "delete"
* Open app/views/topics/index.html.erb and remove these two lines:
```
<td><%= link_to 'Show', topic %></td>
<td><%= link_to 'Edit', edit_topic_path(topic) %></td>
```
* Change the line with the word 'Destroy' to this:
```
<td><%= link_to 'Delete', topic, method: :delete, data: { confirm: 'Are you sure?' } %></td>
```
* Now save your file and try reloading in your browser to see the changes

*The two links we removed were show and edit. We did this because the title now links*
*to the show page and from the show page you can reach the edit page.The second change*
*we made was to make the link text 'Delete' instead of 'Destroy'.*

### Push your changes to Github and then Heroku, as we did previously.


# Review Everything We've Learned So Far. Just Breathe. 


## Let's Make it Shinier, Shall We? 
### Bootstrap Makes *EVERYTHING* Better
* Activity:  Build a house (Cotton vs toothpicks and marshmallows) 
You'd really like this to look better, right?  I know I would!  
Head to this [Bootstrap link](https://github.com/seyhunak/twitter-bootstrap-rails) and let's
take a look at a good way to make that process magically easy! 
 


## Steps to install Bootstrap on your Rails App: 
* Add the following to your Gemfile: 
```
gem "twitter-bootstrap-rails"
```
* Next, Type the following into your terminal: 
```
rails generate bootstrap:install static

```
* Now, go take a look at your application.css.scss file, and you should see the following now there: 
```
//= require twitter/bootstrap

```
* Generating the install placed that statement there so that application file will now use Twitter Bootstrap with your app! 
* Here is some light reading: [Documentation](http://www.rubydoc.info/gems/twitter-bootstrap-rails/3.2.2)
* Next, go to each "topic" view and modify the code a bit.  Add:
```
<div class="container">
```
to the top of each file,  and 
```
</div>
```
to the bottom of each file.  
It should look like this: 
```
<div class="container">
  <p id="notice"><%= notice %></p>
  <h1>Listing Topics</h1>
        <thead>
            <tr>
              <th>Title</th>
              <th>Description</th>
              <th colspan="3"></th>
            </tr>
        </thead>

        <tbody>
          <% @topics.each do |topic| %>
            <tr>
              <td><%= topic.title %></td>
              <td><%= topic.description %></td>
              <td><%= pluralize(topic.votes.count, "vote") %></td>
              <td><%= button_to '+1', upvote_topic_path(topic), method: :post %></td>
              <td><%= link_to 'Show', topic %></td>
              <td><%= link_to 'Edit', edit_topic_path(topic) %></td>
              <td><%= link_to 'Destroy', topic, method: :delete, data: { confirm: 'Are you sure?' } %></td>
            </tr>
          <% end %>
    </table>


  <br>

 <button><%= link_to 'New Topic', new_topic_path %></button>

</div>
```
It's like a pair of book ends!
The container adds some attributes from the Bootstrap library, like padding and spacing. 


* Now, Let's play a bit! Go to your topics.css file and add the following import command and style code and Save:  
```
@import url('https://fonts.googleapis.com/css?family=Amatic+SC:400,700');
 
 body, td {
  color: #333;
  font-family: 'Amatic SC', cursive;
  font-size: 18px;
  line-height: 30px;
}
```
* Go Restart your app in C9
* Now, go to your topics page and take a look!  
* HEY! Cool!!! What happened here?  

### First, We installed a gem that allows Rails to use Bootstrap, which is a front end framework! 
* We added the gem and installed it. 
* Then, we added a fun google font to our topics! You can play with other [fonts](https://www.google.com/fonts#)!

### Push your changes to Github and then Heroku, as we did previously. 


# Congratulations! 
## You've just created, styled, and deployed your very first piece of software! 
*Remember: This is a journey!* 
*Every cool thing you learn from here on out simply makes you a better developer!*
### *Welcome to the club!* 

 
### CSS Intro
 * Video/Activity about how CSS works.  
 * Individual work on styling. 

## Personlize
## Catch Up Week or extra credit activities!  
* Add a downvote button that does the opposite of what the upvote button does
* Add an 'about' page, linked from the bottom of the topics list.
* Link back to the Topics list from the About page so users don't get stranded.

<!--A bit more Advanced: -->
<!--* Sort topics by their number of votes-->
<!--* Create upvote and downvote methods in the Topic model and use those in the topics controller instead directly modifying the topics votes-->

## Final Workshop
* Wrap Up
* Show & Tell
* Exhange Githubs and Social Information to Stay in Touch
* Parents invited for small reception

### Next up at Lvl\U/p is a series that builds on this foundation series to create 1 of 3 more advanced Apps
### Students will be working in Teams of Developers to complete the apps.(In depth GitHub etc)
### Feel free to take your app further on your own, and peruse the resources below! 

# Resources: 
* [Railsbridge on Github](https://github.com/railsbridge/docs): Amazing folks, without whom Lvl\U/p wouldn't exist! 
* [Rails Guides](http://guides.rubyonrails.org/): The mother ship for Rails!  
* [Getting Started with Bootstrap!](http://getbootstrap.com/getting-started/#examples): This is a great place for example code for learning to create more fun stuff on that front end!
* [Bootstrap CSS Page](http://getbootstrap.com/css/#overview): Global CSS settings, fundamental HTML elements styled and enhanced with extensible classes, and an advanced grid system. 
* [Unsplash](https://unsplash.com/): free, high-quality photos that you can download and use! 
* [GitHub Help](https://help.github.com/categories/using-git/): Git...Help. That easy! 
* [Codecademy](https://www.codecademy.com/): A free site to help you learn and practice coding! 
* [Stack Overflow](http://stackoverflow.com/): This is a great place to ask questions and get answers. 
* [Simple Daily Git Workflow: An Excellent Resource!](http://image.slidesharecdn.com/dcnyc10-gitingear-120510030924-phpapp02/95/git-in-gear-how-to-track-changes-travel-back-in-time-and-code-nicely-with-others-30-638.jpg?cb=1397421717)
* [Heroku Dev Center: Help and Answers!](https://devcenter.heroku.com/)
* [Harvard's Popular CS 50](https://cs50.harvard.edu/): A fabulous online open course on Computer Science! Highly Recommended! 






