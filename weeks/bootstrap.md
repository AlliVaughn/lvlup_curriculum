# Let's add Bootstrap Front End framework to our project, so it looks nicer! 

1. First, let's add a gem to our gemfile! 

```
source 'https://rails-assets.org' do
  gem 'rails-assets-bootstrap'
end
```

In terminal, run:  

```
bundle install
```

Rename the file ```app/assets/stylesheets/application.css``` to ```app/assets/stylesheets/application.scss```  

Erase what is there, and add: 

```
@import "bootstrap";
@import "bootstrap-overrides";



```

Next, create a file called ``` app/assets/stylesheets/bootstrap-overrides.scss``` but don't add anythhing there yet. 

Add the following to your ```app/assets/javascipts/application.js``` file, and erase what's there currently:

```
//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require_tree .
//= require bootstrap
```  

Ok. What did we just do?  We added a gem that helps us manage our rails assets and bootstrap front end framework, and configured the application to do just that.  

All that remains is to learn and play with bootstrap, CSS and HTML classes!  

When we are ready to push it to our live site on heroku, we need to run: 

```
rake assets:precompile RAILS_ENV=production
```
Then push it to github and then to  Heroku. 

Voila!  



