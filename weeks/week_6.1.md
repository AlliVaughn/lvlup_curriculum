![logo](https://github.com/AlliVaughn/lvlup_curriculum/raw/master/images/logo.png)
=================================

## Make The Topic Title A Link & Clean Up Links On The Topics List
## [Make The Topic Title A Link](http://docs.railsbridge.org/intro-to-rails/make_the_topic_title_a_link)

Let's go ahead and dispense with the awkward by making the title a link and when it's clicked, show the description.
* Let's start by removing the description. Open app/views/topics/index.html.erb and delete the line that looks like this:
```
<td><%= topic.description %></td>
```
* Also delete the line that looks like this:
```
<th>Description</th>
```
*If you save and try to load it in the browser you should see that the description no longer appears.*

* Now make the title a link by editing 
```
app/views/topics/index.html.erb
```
(again) and replacing this line:
```
<td><%= topic.title %></td>
```
with this:  
```
<td><%= link_to topic.title, topic %></td>
```
* Confirm your changes! 

Explanation
```
<td><%= topic.description %></td>
```
This line was getting the description using .description and just printing it out.

```
<th>Description</th>
```

<th> stands for table header and everything between these tags
```
<th> </th>
```
 was being printed as a table header (bold). We removed it since we removed the description and it would look funny to have the header and the wrong thing below it.

##  Push your changes to Github and then Heroku, as we did previously. 
## [Clean Up Links On The Topics List](http://docs.railsbridge.org/intro-to-rails/clean_up_links_on_the_topics_list)


* Our page is cluttered with some unnecessary links!
* Let's clean those up by removing the "show" and "edit" links and changing "destroy" to "delete"
* Open app/views/topics/index.html.erb and remove these two lines:
```
<td><%= link_to 'Show', topic %></td>
<td><%= link_to 'Edit', edit_topic_path(topic) %></td>
```
* Change the line with the word 'Destroy' to this:
```
<td><%= link_to 'Delete', topic, method: :delete, data: { confirm: 'Are you sure?' } %></td>
```
* Now save your file and try reloading in your browser to see the changes

*The two links we removed were show and edit. We did this because the title now links*
*to the show page and from the show page you can reach the edit page.The second change*
*we made was to make the link text 'Delete' instead of 'Destroy'.*

### Push your changes to Github and then Heroku, as we did previously.

[OVERVIEW](overview.md)