## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
A cookie is a collection of your saved state so that a webpage can remember you. It is usually represented by text files.
* What’s the difference between a session and a cookie?
  A session is a hash and can persists longer than a cookie. 
* What’s a flash and when do you want to use flashes?
  Flashes are messages that appear on your webpage when a specific action is completed. 
* Why do people say “HTTP is stateless”?
  Because without the use of cookies and sessions it would not be able to remember who you were. 
* What’s authentication? Explain.
  Authentication is the process of verifying that a user is who they say they are. 
* What’s the difference between authentication and authorization?
  Authentication is the verification process whereas authorization is the process of granting special permissions to these verified users. 
* What’s a before filter?
  A before filter tells your controller(s) to do a specific thing before a specific action or set of actions. 
* How do we keep track of a user once they’ve logged in?
  Adding a key-value pair to the session hash, of user_id => :id
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  You would want to namespace a resource when those resources require specific authorization. 
* At a high level, what tools can you use to implement authorization? How would you use them?
  Before_action verify that the person is a user or a specific type of user. Or int he view have conditions as to when to display certain content. 
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  Enum's correlate a certain word with an indexed number. This will allow you to save data space on your files by indicating the value with numbers rather than the value itself. You declare an enum inside of your model. 
* What are some strategies you can use to keep your views DRY?
Extracting any activerecord queries into methods on the model. You can also use partials for anything that is repeated across multiple views. 
