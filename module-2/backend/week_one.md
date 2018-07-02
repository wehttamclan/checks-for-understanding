## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
post - creates content
get - reads/fetches content
put - adds to existing content
patch - edits content
delete - deletes content

2. What is Sinatra?
Sinatra is a lightweight framework for creating apps.

3. What is MVC?
Model, View, Control is a data structure for creating apps.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We follow conventions in Sinatra so that we can collaborate with others.  

5. What types of variables are accessible in our view templates without explicitly passing them?
instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    erb :index
  end
  ```

8. What's the purpose of ERB?
ERB incorporates the use of ruby code in html code to render html pages.

9. Why do I need a development AND test database?
test databases are constantly created, edited, destroyed, are much lighter in order to show what functionality development databases will display within the same app.

10. What is CRUD and why is it important?
Create, Read, Update, Delete are the four basic functions that allow you to fully use databases.  They allow apps to make use of data.

11. What does HTTP stand for?
hypertest transfer protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
With the tags <%> and <%=>.  One allows ruby variables to be called and one allows for ruby variables to be printed.

13. What's an ORM? What does it do?
Object Relational Mapper gives access to functionality between systems/languages that otherwise wouldn't be able to work compatibly.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ERB

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
GET '/' - homepage with links to menu, menu items, and orders
GET '/menu' - page for the menu with links to food items
GET '/menu/:item' - page for specific food items with item info
GET '/order' - page with an order form
PUT '/order' - submits form with order info
GET '/order/confirmation' - landing page for order info and confirmation
GET '/contact_us' - contact information

16. What's a migration?
A migration takes ruby code and creates schemas for database tables with it.

17. When you create a migration, does it automatically modify your database?
No, it simply sets up the rules to do so.

18. How does a model relate to a database?
Given a class name it creates a table with that name and in the class there are associations set up and methods written to be able manipulate data in the database.

19. What is the difference between `#new` and `#create`?
new instantiates an object where create will instantiate the object and save it as a row in the associated table.


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

CSV.foreach('./“films.csv', headers: true, header_converters: :symbol) do |film|
 Film.create(id: film[:id],
             title: film[:title],
             description: film[:description])
end

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies] << 'granola bar'

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation - hiding data from public access
Abstraction - being able to interact with classes and their methods without having to know/understand the implementation/logic within those methods.
Inheritance - sets up a super class structure where classes can inherit functionality from their super classes.
Polymorphism - I don't know what this is.

### Self Assessment:
Choose One: (erase the others)
* I was able to answer every question without relying on outside resources
(except number 22.  I hadn't ever heard of 'the 4 Principles of OOP')

Choose One:
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
A little from column A, a little from column B.
