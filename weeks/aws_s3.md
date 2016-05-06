Head over to [AWS Cloud Services](https://aws.amazon.com/) and let's create an account, and then a bucket to store our image files!

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







