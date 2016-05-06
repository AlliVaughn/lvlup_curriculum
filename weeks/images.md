# [Steps to use Imagemagick and Paperclip to add Images with posts.](http://robmclarty.com/blog/how-to-install-image-magick-and-setup-paperclip)
[A video](https://www.youtube.com/watch?v=Z5W-Y3aROVE) 
[Instagram](https://www.devwalks.com/lets-build-instagram-in-rails-part-1/)

Let's talk through this! We need to install software that can upload images, just as you can  upload images on Instagram and Facebook. Next, we need a gem that will attach those images, in this case to our topics!  ( You may want to do avatar pics for users, eventually!) We then need to update the  model and controller to be able to work with the images. Finally,  we need to style our views to be able to display our images in a jaunty way! ( More on that step soon!)

1. We need to install software that can upload images, just as you can  upload images on Instagram and Facebook.

First, Create a branch by typing the following in your C9 ubuntu terminal: 

```
git checkout -b images
```
**You've switched to a branch called images now!**


Then, In your terminal:

```
sudo apt-get update
```
Then: 

```
sudo apt-get install imagemagick 
sudo apt-get install imagemagick -y
```

(First, You are installing Uploader Package for the images.)

2. Next, we need a gem that will attach those images, in this case to our topics!

Install the Paperclip gem: 

In your gemfile, add: 

``` 
gem 'paperclip', '~> 4.3.6'
```
Some reading at Github on [Paperclip](https://github.com/thoughtbot/paperclip)

Save it, and then in terminal:  

```
bundle install
```
3.  We then need to update the model and controller to be able to work with the images.

To your Topics Model, Add: 

```
has_attached_file :image, styles: { :medium => "640x", :small =>"400x" }
validates_attachment_content_type :image, :content_type => /\Aimage\/.*\Z/
```

To your Topics Controller, Add ':image' to your topic params at the bottom: 

```
def topic_params
    params.require(:topic).permit(:title, :description, :image, :upvote)
end
```


4. Now,we need to add an image model to our topics. 
In your ubuntu terminal, let's generate a model.  
```
rails generate paperclip topic image 
```
...and tehn migrate our database. 

```
rake db:migrate
```

5. Now, We will Change our topic input form to accept images and display them in views.  

Add the following code in ```app/views/topics/_form.html.erb```, so that the  line looks identical:  
```
<%= form_for(@topic, html: {multipart: true, image:true }) do |f| %>
```
The ```multipart: true, image:true``` part sends a message for the form to be able to accept our image upload. 

then, add an image input label and field, like your title fields!  In fact, you can copy and paste those, and change them if you like! 

```
<%= f.label :image %>
<%= f.file_field :image %>
```

6. At this point, if you start your  server, and create a new topic, you will be able to  grab a picture and upload it, but the  show view will not display it. Let's fix that!  

In ```app/views/topics/show.html.erb``` and ```app/views/topics/show.html.erb```, add the following code in order to refer to that image object we've made and uploaded: 

```
<%= image_tag @topic.image.url(:medium) %>
```

NOW go ahead and upload, and see what happens...

7. Ok!  Let's go ahead and save this, push this to github and push to heroku master.  We'll need to :  

```
git add . 
```

```
git commit -m'added imagemagick file uploader, paperclip gem, an image attribute to Topic model and migrated, updated the topic controller to include the  image param at the  bottom,   and changed the topic/_form and topic/show and index views to reflect this'
```

Now, checkout your  master branch by typing: 

```
git checkout master 
```

Now merge the two: 

```
git merge images
```
Check to see your  status:  

```
git status
```

It should say that you are on branch Master with nothing to commit.  

Now push to github: 

```
git push origin master 
```
When that's done:  

```
git push heroku master
```


