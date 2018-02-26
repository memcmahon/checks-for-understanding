Questions from Week 5:
1. How do we make flash messages display on a page?
  * Add a flash message to the action where that flash should be displayed, and include the flash type on the view for that page.

2. Where is cart information/temporary information usually stored?
  * a session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  * You may not want to store carts in your database to save on storage.  You might want to, if you want users to be able to log back in to see a cart that they had started in another session.

4. What is the purpose of the asset pipeline?
  * The asset pipeline prepares assets to be used in a production environment.

5. Why do we precompile our assets?
  * We precompile to compress and combine assets into a single location.

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
  # links all stylesheets in the application.
<%= javascript_include_tag "application" %>
  # links all javascript files in the application, this and the tag above improve the flow of assets when deployed to production.
<%= image_tag "rails.png" %>
  # links images by their fingerprint
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  * Summary of the application
  * Instructions on how to use the application
  * Code snippets to illustrate installation and use
  * links to related resources
  
  A readme is beneficial so that other's can easily understand and use the application.

8. What are the top four accessibility issues that we as developers should be aware of?
  * Blindness
  * Color blindness
  * Cognition
  * Mobility

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  * before_save is a callback.  You would use it in one or more of your application controllers.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)

scope :active, -> { where(active: true) }
```

11. What is the difference between a scope and a class method?
  * scopes and class methods can accomplish the same tasks, but scope allows for a simplified way of returning a list of objects.


Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4? 
  `given[:cart]["48"] = 4`
  12b. How would you increase the quantity of item 29? 
  `given[:cart]["29"] += 1`
  12c. How would you find out how many items your user is thinking about purchasing?
  `given[:cart].values.sum`
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?
  * polymorphism is the idea that you can use the same method name for multiple classes and get different results, depending on the class that the method is called on.  Duck-typing is a concept used to explain polymorphism.  We use ducktyping often in rails applications in the applicaition controllers (index, show, etc...) or, possibly in different models.
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
`number.gsub(/[()]/, "").gsub(/[ -]/, ".")`
