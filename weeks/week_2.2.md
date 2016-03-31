![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Add The Project To A Git Repo
This cloud environment is nifty, but, um, how do we *keep* our stuff?  Where will it live? 
Imagine your project is a cold puppy outdoors in the Winter... That's sad, right? 
Let's help our furry friend. 

* Activity:  Jenga 

* We will use this resource: [Push your C9 Project to GitHub](http://lepidllama.net/blog/how-to-push-an-existing-cloud9-project-to-github/)
* Open gitHub and Sign in, and place the tab next to your C9 dashboard tab
* In C9 dashboard ( make sure you are on your dashboard!), click "settings" (the gear) button on the right. 
* In the menu to the left click on "connected services". 
* click "activate" next to gitHub and follow instructions to connect **OR,  If you've already connected gitHub, you can skip this step.** 
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
* Open your C9 project window, and go to the terminal. **Set your git config username:**```git config --global user.name "Your Git Name Here"```
* Next, also in the terminal, Set your git config email (which should match your github account email):```git config --global user.email "your_email@example.com"```
* Now, Make your current directory a git repository by typing: ```git init```
* Using the SSH link you copied from your gitHub repository, add the remote repository as the origin:```git remote add origin git@github.com:yourname/yourrepository.git```
* Add your files and commits, as you normally would:```git add .``` and then ```git commit -m "First commit"```
* Push your changes:```git push -u origin master```
* Go look at your gitHub repo and refresh:  MAGICAL!  You now have a full copy of all of your work from C9 on a gitHub repo! 
* [Simple Daily Git Workflow: An Excellent Resource!](http://image.slidesharecdn.com/dcnyc10-gitingear-120510030924-phpapp02/95/git-in-gear-how-to-track-changes-travel-back-in-time-and-code-nicely-with-others-30-638.jpg?cb=1397421717)

*Phew! That was a lot! Well Done, You! Let's get back to our project!* 

[OVERVIEW](overview.md)