![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================
## [Allow People To Vote](http://docs.railsbridge.org/intro-to-rails/allow_people_to_vote)

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
