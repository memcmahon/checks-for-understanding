## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET - used to Read information
  * POST - for Creating records
  * PUT - used to Update complete records
  * PATCH - used to Update partial records
  * Delete - for deleting entire records
2. What is Sinatra?
  * Sinatra is a language that is used to create server responses for web applications.
4. What is MVC?
  * Model, View, Controller
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  * Conventions allow for better readability for other developers and our future selves.
6. What types of variables are accessible in our view templates without explicitly passing them?
  * Instance variables which are set in the controller.
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    name = "Mr. Ed"
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
  * ERB is used to incorporate ruby emthods into the html files directly.
10. Why do I need a development AND test database?
  * test databases keep the integrity of the development (and production) databases while still being able to test the full functionality of the database.
11. What is CRUD and why is it important?
  * CRUD stands for Create, Read, Update and Delete.  These are the actions that describe all events that the controller performs with the database.
12. What does HTTP stand for? 
  * Hypertext Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  * <% %> - used for interpolating non-viewable Ruby
  * <%= %> - used for interpolating Ruby which will be viewable in the html document (when rendered)
14. What's an ORM?
  * Object Relational Map - a framework for organizing a working with a relational database.
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * ActiveRecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  * GET index - view all restaurants
  * GET new - see new record form
  * POST restaurant - create a new restaurant
  * GET edit - see edit record form
  * PUT restaurant - edit an existing restaurant
  * GET restaurant - see an individual restaurant
  * DELETE restaurant - delete a single restaurant
17. What's a migration? 
  * The blueprint for the tables in your database.
18. When you create a migration, does it automatically modify your database?
  * no, you must also run the migrations.
19. How does a model relate to a database?
  * a model translates and manipulates information within the database.
20. What is the difference between `#new` and `#create`?
  * #new instantiates a new instance of an item.  #create instantiates the item and saves it to the database.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  * ```ruby
    films = CSV.open("films.csv", headers: true, header_converters: :symbol)
    films.each do |row|
      Film.create(id: row[:id], title: row[:title], description: row[:description])
     end
     ```
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
  * ```ruby
    activities[:hiking][:supplies] << "granola"
    ```
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  * Encapsulation - containing functionality within a set method or object.
  * Abstraction - 'hiding' data points within something eles, like a variable or constant.
  * Inheritance - having access to the functionality of other classes through a parent-child-like relationship.
  * Polymorphism - the ability to override existing methods - monkey-patching could be an example.


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
