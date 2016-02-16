![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Let's Make it Shinier, Shall We? 
## Bootstrap Makes *EVERYTHING* Better
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
* Here is some light reading: 
[Documentation](http://www.rubydoc.info/gems/twitter-bootstrap-rails/3.2.2)