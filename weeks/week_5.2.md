![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

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