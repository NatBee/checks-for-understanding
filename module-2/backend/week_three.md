## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

rails new app_name

2. What do Models generally inherit from in rails?

Models generally inherit from ActiveRecord::Base

3. What do Controllers generally inherit from in a rails project?

Class inherits from ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources: :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes -- it displays all of the routes in the app and it gives you the route helpers, uri, and controller action.

6. What is an example of a route helper? When would you use them?

horses_path is an example of a route helper and it is a built in method in rails. You use them everytime you use rails and you are rendering information to the browser. 

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

Both tells rails where to look in the controller to find the correct method. _url is the absolute path and _path is the relative path. 

8. What are strong params and why are the necessary?

Strong params explicitly pass only the info we want to pass and safe guard against a user editing or adding params to your hash and accessing your database.

9. What role does `form_for` play in helping us create our forms?

It is a method that allows a user to to create and save a new item in the databse. It creates a from from information.

10. How does `form_for` know where to submit the user's input?

It is connected to the attributes of the model. It allow it to look for the verb so that it finds the right path. It provides validation that you're saying the right thing. 

11. Create a form using a `form_for` helper to create a new `Horse`. 

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?

We want to validate our models so that when data is being added to the database, all necessary attributes are being populated and are in the appropriate format.
