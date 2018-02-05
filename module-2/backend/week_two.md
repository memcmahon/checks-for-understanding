## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  * ActiceRecord is a DSL which helps with communicating with and manipulating a database.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  * Team.all, Team.count, Team.sum(attribute), Team.average(attribute), Team.find(id), Team.where(attribute).  We have access to these methods because they are inherited from ActiveRecord

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  * Team.find(4).name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  * Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  * Teachers will have many students and students will have many teachers.  There will be a join table in the database to caputure this relationship.
6. Define foreign key, primary key, and schema.
  * Foreign key is a column on a database which relates directly to the primary id of another table.  The primary id is the unique identifier for each record on the table.  The schema is a visable representation of the database tables.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  * A foriegn key is an attribute of a record on one table that directly corresponsds with the primary key of a record on a second table; this forms relationships between the two tables.
8. What are the parts of an HTTP response?
  * Status, Header, Body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
