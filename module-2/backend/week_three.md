## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  rails new
2. What do Models generally inherit from in rails?
  ApplicationRecord which in turn inherits from ActiveRecord.
3. What do Controllers generally inherit from in a rails project?
  ApplicationController which in turn inherits from ActionController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
In your config/routes.rb file you would add the following line:
  resources :horses, only: :show
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes provies your with your path prefixes, matching verbs, URI pattern and controller#action combo.
6. What is an example of a route helper? When would you use them?
  company_path(company) would be useful if you wanted to go to the individual company page.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  '_url' includes the protocol as well as the where the site is hosted. _path will only give you the path. 
8. What are strong params and why are the necessary?
  Strong params take the form of a method in the controller class. We use strong params to prevent any errors through mass assigning all of the attributes of a particular record.
9. What role does `form_for` play in helping us create our forms?
  It will tell rails that we need a form on this particular page. It will also look for a corresponding model.
10. How does `form_for` know where to submit the user's input?
  form_for can take any number of arguments that will then be used to point to a specific route
11. Create a form using a `form_for` helper to create a new `Horse`.
  <%= form_for [@horse] do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>

    <%= f.submit %>
<% end %>
12. Why do we want to validate our models?
To make sure that our record is being made completely, that none of it's attributes are left empty (particularly those attributes that are necessary to the creation of a record)
