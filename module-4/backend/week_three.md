## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
Node is a framework for developing serverside javascript. It will allow you to run javascript without a client. 
2. What is Express? What is Express similar to in the Ruby world?
Express is a backened framework that will allow you to create models and controllers. It is analogous to Sinatra in the ruby world.  
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
 Routes are set up using the server.js file which contains all of the configuration for an express/node backend. It will also contain all of the routes that your API uses. 
 
`const express = require('express')
const app = express()
const bodyParser = require('body-parser')
const mealController = require('./lib/controllers/meal')
const foodController = require('./lib/controllers/food')

const environment = process.env.NODE_ENV || 'development';
const configuration = require('./knexfile')[environment];
const database = require('knex')(configuration);

const cors = require('cors')

const path = require('path')

app.set('port', process.env.PORT || 3000)
app.locals.title = 'Quantified Self'
app.use(bodyParser.json())
app.use(bodyParser.urlencoded({ extended: true }))
app.use(express.static(path.join(__dirname, 'public')));

app.get('/', function(request, response){
  response.sendFile(path.join(__dirname + '/index.html'))
})

if(!module.parent) {
  app.listen(app.get('port'), function() {
    console.log(app.locals.title + " is running on " + app.get('port') + ".")
  })
}

module.exports = app
`

4. What do we use Knex for?
 We use Knex is a SQL framework for making database queries within a node/express API. 
5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
With you server.js file acting as the routes file you can then create a directory for your controllers which will setup the server connection and then models that will interact with the SQL database. 
6. How do you execute raw SQL in node?
Using Knex, you can execute raw sql with the following syntax: knex.database.raw('Your SQL goes here')
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
One advantage is that you can seprate your codebases allowing for easier debugging, where you can identify problematic code much easier. One disadvantage is that you will then have to setup CORS for your requests, CORS standing for cross origin resource sharing. 

#### Review  

8. Describe DNS. 
DNS stands for Domain Name Service and is the system that we use to resolve domain name requests. For example: if you were to go to google.com (provided you don't have the address in a memory cache) your request would go to the DNS to figure out the IP address to google.com.
9. What does writing clean code mean to you?
To me writing clean code means that all functionality is modular and reusable for other areas of code. It also means that you are seperating all of the functionality into appropriate files, allowing for clearer organization. 
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality? If I were building an app that models hotels I would use the following 3 classes: customer(user), room, floor. A customer to model the people who will be reserving rooms, a room to model when a room has been reserved and when and finally a floor to organize rooms by floor and allow for easy booking of adjacent rooms. 
