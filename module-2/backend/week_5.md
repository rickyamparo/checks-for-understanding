1. How do we make flash messages display on a page?
I would add the following code to the application.html.erb:
    <% flash.each do |name, msg| %>
      <%= content_tag :div, raw(msg), class: name %>
    <% end %>

    What this is doing is iterating through the flash hash, calling the key name and value msg. Then it will display each of the msg attached to the specific name(key)

2. Where is cart information/temporary information usually stored?
  In a cart Plain Old Ruby Object (PORO).

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information? We might want to persist that information if a person logs in and logs out, and they can still view everything in their cart. The problem though is that we then have to start creating a new record in the carts database every time a person changes their cart, so that the web app can pull up this persisting cart. This can get pretty unwieldy as far as databases go.

4. What is the purpose of the asset pipeline?
  The asset pipeline is a framework for modifying your assests(usually through minifying and concatenation) that will allow you to present those assets in the most efficient means possible.

5. Why do we precompile our assets?
  To minimize the amount of requests that our server would have to conduct. Rather than requesting each individual asset it requests them all together.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
  Access the style sheet named application anywhere in the file where you include this.
<%= javascript_include_tag "application" %>
  Access the JS page named application anywhere in the file where you include this tag.
<%= image_tag "rails.png" %>
inserts an image named rails.png in the page where this tag was included.
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project? Great readmes include table of contents(ESSENTIAL), description of how to use this app/gem, how to troubleshoot common errors, a "mission statement", information about how to report a bug, a section about the DSL to your gem. The benefits of updating your readme as you move through your project is that it becomes a sort of tracker to your project, providing you will a map of what you app/gem can currently do.

8. What are the top four accessibility issues that we as developers should be aware of?
  The four main accessibility issues that developers should be aware of are Visual, Mobility, Cognition and Hearing needs.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
This is an example of a call_back. We would typically find a before_save in a controller file.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
User.where(active: true)

11. What is the difference between a scope and a class method?
A scope method works on a smaller subset of a collection. Class methods work on the entirety of the collection. 
