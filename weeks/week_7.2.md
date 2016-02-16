![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Bootstrap Basics
* Next, go to each "topic" view and modify the code a bit.  Add:
```
<div class="container">
```
to the top of each file,  and 
```
</div>
```
to the bottom of each file.  
It should look like this: 
```
<div class="container">
  <p id="notice"><%= notice %></p>
  <h1>Listing Topics</h1>
        <thead>
            <tr>
              <th>Title</th>
              <th>Description</th>
              <th colspan="3"></th>
            </tr>
        </thead>

        <tbody>
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
    </table>


  <br>

 <button><%= link_to 'New Topic', new_topic_path %></button>

</div>
```
It's like a pair of book ends!
The container adds some attributes from the Bootstrap library, like padding and spacing. 


* Now, Let's play a bit! Go to your topics.css file and add the following import command and style code and Save:  
```
@import url('https://fonts.googleapis.com/css?family=Amatic+SC:400,700');
 
 body, td {
  color: #333;
  font-family: 'Amatic SC', cursive;
  font-size: 18px;
  line-height: 30px;
}
```
* Go Restart your app in C9
* Now, go to your topics page and take a look!  
* HEY! Cool!!! What happened here?  

### First, We installed a gem that allows Rails to use Bootstrap, which is a front end framework! 
* We added the gem and installed it. 
* Then, we added a fun google font to our topics! You can play with other [fonts](https://www.google.com/fonts#)!

## Push your changes to Github and then Heroku, as we did previously. 


# Congratulations! 
## You've just created, styled, and deployed your very first piece of software! 
*Remember: This is a journey!* 
*Every cool thing you learn from here on out simply makes you a more knowledgeable developer!*

### *Welcome to the club!* 
