## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  * rails g new project_name -T -d="postgresql"
2. What do Models generally inherit from in rails?
  * ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
  * ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  * get 'horse/:id', to: 'horses#show', as: 'horse'
5. What rake task is useful when looking at routes, and what information does it give you?
  * rake routes - this returns all available routes as previx, verb, uri pattern and controller#action combinations.
6. What is an example of a route helper? When would you use them?
  * route helpers are the key-word methods that correspond to URIs, such as items_path.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  * I think they return the same thing - a full URI
8. What are strong params and why are they necessary?
  * strong params are a private method used to control what attributes users have access to changing.
9. What role does `form_for` play in helping us create our forms?
  * form_for is a tool to help create html forms.
10. How does `form_for` know where to submit the user's input?
  * based on the action#control where the form was initiated.
11. Create a form using a `form_for` helper to create a new `Horse`. 
  ```ruby
  <%= form_for @horse do |f| %>
    <%= f.label :breed %>
    <%= f.text_field :breed %>
    
    <%= f.label :name %>
    <%= f.text_field :name %>
    
    <%= f.submit %>
  <% end %>
  ```
12. Why do we want to validate our models?
  * Validations ensure that all of our resources are created correctly.
