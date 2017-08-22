## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
Get - reading information
Post - Create information
Put - Replace information
Patch - Modify information
Delete - Delete information
2. What is Sinatra?
Sintra is a web-applicaiton framework for ruby.
3. What is MVC?
MVC is a specific model for designing web-applications. It stands for Models, views, controller.
4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We follow conventions for the same reason that we follow conventions in software development; we need our code to be easily understood by other developers. Additionally, in the case of Sinatra routes, it is a way that all websites can standardize the common practices of creating, reading, updating and deleting information.
5. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables
6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    name = "Mr. Ed"
    erb :index :locals => name: name
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
The purpose of Embedded Ruby is to insert ruby into a text document, usually into an HTML page.
10. Why do I need a development AND test database?
You need to have two databases so that you can separate your your development and testing suite. For testing you would probably want to use fixtures to cut down on the time that your tests take. In development you might want to use a fuller database to closely mirror what your application will be using.
11. What's responsive design?
Responsive design is opposed to fixed design. In my mind, a fixed design would be the same across all different platforms and clients. Whereas a responsive design changes dynamically to fit the needs of each individual client/platform. An example would be a screen that would resize itself across smartphones, desktops etc.
12. What is CRUD and why is it important?
CRUD stands for Create, Read, Update, and Delete. This is important because these describes the way in which a user can interact with a given database.
13. What does HTTP stand for?
  Hypertext Transfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
15. What's an ORM?
Object Relational Mapper, used to create uniform databases from mismatched datasets.
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
Active Record, because it's awesome.
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  get '/restaurant'
  get '/restaurant/:id'
  get '/restaurant/new'
  post '/restaurant'
  get '/restaurant/:id/edit'
  put '/restaurant/:id'
  Delete '/restaurant/:id'
18. What's a migration?
It is a way of altering the structure of your database.
19. When you create a migration, does it automatically modify your database?
 No it does not automatically modify your database, but rather your schema.
20. How does a model relate to a database?
  Through the inheritance of ActiveRecord methods.
21. What's the difference between agile workflow and waterfall method?
  Waterfall is the traditional model where people work on everything all at once. Agile compartmentalizes the work needed into smaller chunks. By doing this, the team has many more points of feedback and are able to make more changes during the development as opposed to the end of development.
22. What is the difference between `#new` and `#create`?
New only creates a new instance of your model whereas create makes a new instance and then saves it to the database.
