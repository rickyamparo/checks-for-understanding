## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
The most useful thing I learned over intermission was how to separate functions and then call them from each other. 
2. What are some tools to help debug JavaScript code?
Debugger, alert, console.log, pryjs. 
3. What are some tools you need in order to unit test your JavaScript?
Mocha, Chai
4. What is the syntax for invoking a function?
  functionName(param)
5. What is CORS?
  Cross Origin Resource Sharing
6. How do we enable CORS?
  I beleive that when you are making an ajax call, you can set the mode to CORS as one of the headers of the request. 
7. What's `this` in JavaScript?
  This is contextual identifier based on your scope. 
8. What is Webpack and why is it useful?
  Webpack is a tool to consolidate all of your javascript files. It also performs useful functions such as transcompiling and minifying your code. 
9. When/why do you want to use event delegation?
  When you have a specific event that needs to occure as part of another event. 
10. What's `npm` and what do we use it for?
  Node Package manager. We use it as a means of managing all of the node_modules that we've installed for a specific project or globally. 

#### Review  
11. What's the MVC design pattern? Describe each part of MVC.
  MVC stands for Model, View, Controller and it is a design pattern for web apps. By using this design pattern you are able to separate the different logics into their respective areas and have them communicate with each other. 
12. What are a few ways to optimize a Rails application?
  One way to optimize rails is to make sure that you are indexing your databases as that will decrease your query times. Another way to optimize rails is to know the difference between joins and includes and when to use them. 
13. What's a background worker? When would we want to use a background worker?
A background worker will execute a set of code independent of what is occuring at the user interface level. You can use background workers to run a set of queries that might take some time, but you don't need these queries to allow your web app to work. 
