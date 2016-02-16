
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

 