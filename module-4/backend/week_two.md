## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
  One difference between ES5 and ES6 is that in es5 you declare a variable using `var` whereas in es6 you can use `const` for unmutable values and `let` for mutable values. 
2. What's the difference between asynchronous and synchronous JavaScript? 
  Synchronous Javascript is where you have a singular call stack where all code is executed in order. Asynchronous Javascript is largely due to the fact that browsers give us additional resources to have a call stack for API requests. This way you have continue executing code while your program waits for the API request to resolve. 
3. What are the four pillars of Object Oriented programming?
  Polymorphism, Abstraction, Encapsulation, Inheritence
4. What are some tools available in JavaScript to help you write object oriented code?
  Object contrsuctor functions. These are functions that will return an object with properties defined in the function. You can pass arguments to these functions and they can be set to the properties of the objects. 
5. What are some key concepts to be aware of when refactoring your JavaScript?
  Don't repeat yourself is a good concept to be aware of. Also, a sharp code smell is using set timeouts especially when you can chain promises together. 
6. What's a callback function and what are some reasons when we use/need callback functions?
  A callback function is a function that you specify to run after another function has completed. This is primarily used when making asynchrounous requests so that your program doesn't block while waiting for your request to resolve.
7. What are the different scopes of variables in Javascript? When would you want to define global variables?
  The two primary scopes are global and local. You would want to define a global variable when you have several functions that are going to be using and interacting with that varibale. 
8. What's the difference between `==` and `===` in JavaScript?
    The === operator does not do any type conversion, using this operator 2 will not equal "2" because they are not strictly the same. The == operator will convert types and in the previous example will return true. 
9. Why do front end frameworks exist?
  Front end frameworks exists becuase people do not want to reinvent the wheel every time they create a new project. These frameworks allow javascript developers to shorthand alot of the features of javascript allowing for a much smoother development. 

#### Review  

10. Why do people say "HTTP is stateless"?
  HTTP is described as stateless becuase each request is self-contained with all of the information that it needs. 
11. Describe a RESTful API.
  A RESTful API will only have enpoints that serve resources, tied specifically to a database. 
12. What are some main characteristics of a team following an agile workflow?
  Daily scrum meetings to allow for a smaller feedback look limiting the possibilities of miscommunication. 
13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
  One advantage of using OAuth is that you don't have to worry about storing your users' passwords on your own database. Additionally, you wouldn't have to worry about encrypting the passwords of your users. One disadtange is that if the server where you get your OAuth from goes down, you have no control over when it will come back up. 
