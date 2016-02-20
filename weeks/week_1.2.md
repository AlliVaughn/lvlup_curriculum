![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## [C9 Workspace](http://docs.railsbridge.org/intro-to-rails/getting_started)

## Begin by setting up a new Workspace in C9 IDE: 
* Login to C9
* Create a new workspace 
* Name your Workspace for the app we will create ("your_new_workspace_name")
* Add a description.
* Select the "Ruby" icon to indicate we are using a Ruby IDE. (Note the others! Nifty, eh? ) 
* Click the create workspace button 
* Creating a workspace automagically generates a "Rails New" instance, and names it "your_new_workspace_name" anyway, so no need for that command!

## Environment and Framework Petting Zoo
[Ask Ubuntu](http://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)
 
* Find a terminal like your own command line: open a terminal (if not already open)
* type "ls" to list the contents
* compare to the files you see on the left
* run the project by clicking the "run" button (which is like running "rails s" in a traditional local development environment) 
* click on the url in the terminal window and see your page holder for your app!

## You can see that rails new created a lot directories and files.
The ones we want to focus on today are:

|File Folder    | Purpose                 |
|---------------|-------------------------|
|app/    |Contains the controllers, models, and views for your application. You will do most of your work here.|
|config/ |Configure your application's runtime rules, routes, database, and more.|
|db/     |Shows your current database schema, as well as the database migrations.|
|public/ |The only folder seen to the world as-is. If you put files in here, they will be served directly without any processing by Rails.|
|app/assets|This is where your images, JavaScript, stylesheets (CSS), and other static files should go. Modern Rails apps use something called the Assets Pipeline, which combines all the JavaScript and CSS files in this directory into a single file for speediness.|

There is a lot more that rails new created. Probably enough to fill a book, so we're going to ignore them for now.

[OVERVIEW](overview.md)