## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  Active Record is an ORM that allows us to take varying types of datasets and convert the indiviual pieces of data into ruby objects and relational databases.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
You can call .find(:id) which finds a record matching the id that you pass it, or you can call .create which instantiates a new instances of that class and then saves it to the database. You are able to access these questions because the class is inhereting from the ActiveRecord Class. 

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4).name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

Team.find(4).owner


5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
This will depend of the context of the student-teacher relationship. In an elementary setting, you will probably have a one-to-many relationship, whereas in highschool it could very well be a many-to-many relationship.
6. Define foreign key, primary key, and schema.
Foreign key refers to a key (usually an id) that points to another table where you can obtain further information on the specific record you're on. The primary key is the primray means of locating the record in the table, it usually is an auto-icremented number generated by your computer. Schema a visual representation of these relationships. Additionally, A Schema file is a set of instructions for how your computer should build the databases, and how they relate to each other through foreign and primary keys. 
7. Describe the relationship between a foreign key on one table and a primary key on another table. A foreign key on one table will point to the primary key of another table that contains the rest of the information of the record. 
8. What are the parts of an HTTP response?
A status line, a status code and an optional message body. 


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
 .find finds a record based on its id. 
 .create creates a new model and saves it to the database in one go. 
 .order organizes the table based on the row header that you pass it. 
 .first returns the first record in the table. 
 .last returns the last record in the table.
 
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
Rake DB:drop drops the tables so that you can recreate the table. 
Rake DB:migrate runs all your migration files
rake db:create migration creates a new migration. 

3. What two columns does `t.timestamps null: false` create in our database?
The "created_at" and "updated_at" columns. 

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
see my previous response to this question. 

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

6. Give an example of when you might want to store information besides ids on a join table.
When you need to normalize your database so there isn't so much repition on your tables. 

7. Describe and diagram the relationship between patients and doctors.
This is a many-to-many relationship. A patient can have many doctors (different kinds of doctors) and a doctor most definilty can have many patient (unless she's a private doctor).

8. Describe and diagram the relationship between museums and original_paintings.
  This is a many-to-many relationship since museums can have any original_paitings and original_paintings can be moved around museums and thus has many museums. 
  
9. What could you see in your code that would make you think you might want to create a partial?
Repition, you alwasy want to DRY up your code(don't repeat yourself).
