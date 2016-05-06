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


# So, when we push out to heroku, you'll notice that we can post pictures...for a little while. Then, they seem to disappear.  That's because Heroku isn't storing them permanantly. It isn't set up for that. Let's fix that by setting up Storage with Amazon S3 and our Paperclip gem! 

AWS S3 ACCOUNT: 
[AWS Cloud Services](https://aws.amazon.com/) I am issuing  each of you credentials to an account with LvlUp Workshops, which will give you a bucket to store your image files!  In teh  future, you can create your own account ( you'll need your Mom or Dad to supply a credit card, as they require it to sign up. The service is free for the  first year, but has a small fee after that, and scales with the amount of space you need.) 



1. Let's Update your gemfile with these two gems: 

```
#gem 'paperclip', '~> 4.3.6'

gem 'paperclip', :git=> 'https://github.com/thoughtbot/paperclip', :ref => '523bd46c768226893f23889079a7aa9c73b57d68'

#Amazon Web Services Cloud Storage
gem 'aws-sdk', '< 2.0'
```

Then, in ubuntu terminal, run :  

```
bundle update
```

Why did we change it? Explanation: Gems run into compatability issues at times, and after a round of debugging, I found that this is a nice, stable combination for making sure your cloud storage works!

2. Next, Let's add a configuration to our production environment in order to let heroku know where to look for, put and retrieve our image files on AWS S3. 

In ```app/config/environments/production.rb``` , before the final ```end``` statement, add the following configuration: 

```
config.paperclip_defaults = {
  storage: :s3,
   s3_credentials: {
     bucket: ENV.fetch('S3_BUCKET_NAME'),
     access_key_id: ENV.fetch('AWS_ACCESS_KEY_ID'),
     secret_access_key: ENV.fetch('AWS_SECRET_ACCESS_KEY'),
     s3_region: ENV.fetch('AWS_REGION')
   }
 }
 ```

 Wow! That's a mouthful!  To break this down, we need to configure our production environment, heroku, to be able to communicate with AWS S3 and be able to get and retrieve images.  Otherwise, it isn't much good.
 The  s3 credentials are our variables that allow that handshake to take place.


 3. Why does it simply say a generic placeholder though? 

 GLAD YOU ASKED, Friend! 

 So you want to be kind of careful with your keys. In this era of open source, people can look at the cool environment variables we have and steal them. So what we will do is simply set them on heroku by inputing the  equivalent values on our command line terminal using teh  heroku toolbelt we have, and simply refer to them in our configuration file. 

 To set those values, input each of these lines on your terminal, one at a time and hit return between each.  Make sure to substitute each "your..." value with the actual value of your AWS S3 bucket.  For the ```AWS_REGION``` value, put ```us-east-1```


 ```
$ heroku config:set S3_BUCKET_NAME=your_bucket_name
$ heroku config:set AWS_ACCESS_KEY_ID=your_access_key_id
$ heroku config:set AWS_SECRET_ACCESS_KEY=your_secret_access_key
$ heroku config:set AWS_REGION=your_aws_region  
```

Let's push these files to github, heroku and see what we've made! 









NEXT:  Bootstrap!    





