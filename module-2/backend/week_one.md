## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
GET - returns a thing
PUT - edits an existing thing
POST - creates a new thing
DELETE - deletes a thing
UPDATE - updates a thing
2. What is Sinatra? 
Sinatra is a Ruby framework.
4. What is MVC? 
MVC stands for Model - View - Controller and describes the way that a webpage retrieves data requested from the client. The request comes from the client to the controller to the model, then to the datatbase to retrieve the requested info. The data then goes back through the model to the controller and is output back to the client using view.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We follow convention because Sinatra has many underlying methods and we can access them by following convention without have to know what they all are and what they all are doing. Also Sinatra is looking for things to be in a certain format.
6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = Count.find(params[id:]
    name = "Mr. Ed"
    
    erb :index
    
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB? 
The purpose of ERB is to return and creat the views that will be returned to the client.
10. Why do I need a development AND test database?
You need a development and a test database because we need to be able to test the test and the implementation seperately.
11. What's responsive design?
A responsive design is a design that can replicate the user experiance. 
12. What is CRUD and why is it important?
Create
Read
Update
Delete
CRUD is so important because it is the things we can do with data.
13. What does HTTP stand for? 
HyperText Transsfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<% code %> means render
and 
<%= code %> means execute
15. What's an ORM?
Object Relational Mapping -a tool like ActiveRecord used to map relationships between tables in a database.
16. What's the most commonly used ORM in ruby (Sinatra & Rails)? 
ActiveRecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
GET "/restaurants"  -- see all restaurants
GET "/restaurants/:id" -- see a single restaurant
GET "/restaurants/new" -- use a form to create a new restaurant
POST "/restaurants" -- create new restaurant
GET "/restaurants/edit" -- show form for user to edit a restaurant's info
PUT "/restaurants/:id" -- update edited restaurant info
DELETE "/restaurants/:id" -- deletes restaurant

18. What's a migration? 
A migration alters the structure of a database. You can add/remove a table, or change the name. 
19. When you create a migration, does it automatically modify your database?
No it just creates a shell database and you build the table and populate it executing the migration.
20. How does a model relate to a database?
The model is the instructions for the how the data should be populated in the database table.
21. What's the difference between agile workflow and waterfall method?
Waterfall method is planning a project and working on each phase of the project from start to finish delivering the project as a whole. Analysis, Design, Code, Test is completed in that order and there is very little room for adopting changes from the original plan. 

Agile is completing Analysis, Design, Code, and Waterfall for sprints of the project and delivering a sprint at a time. Agile method allows for a more interactive model and allows the team to more easily refactor and incorporte design changes throughout. Agile also allows more interaction between team and clients and can help the team design software that the client actually wants because they are incorporating feedback.
22. What is the difference between `#new` and `#create`?
'#new' creates a new "thing" but doesn't save it in the database. In order to save a '#new" you would have to follow it with a '#save'.

'#create' creates and saves a new "thing". '#create' does the same thing in one method that '#new' + '#save' does.
