## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
rails new blogger -T -d="postgresql" --skip-turbolinks --skip-spring

2. What do Models generally inherit from in rails?
ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
rake routes

6. What is an example of a route helper? When would you use them?
new_horse_path
use in the controller to redirect_to and in test files

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
path leads you to a predefined path in the routes file
url returns the same path prefixed with the current host, port and path prefix.

8. What are strong params and why are they necessary?
strong params are a private method that allows your controller to have access to params that are necessary.  this is a security feature of rails.

9. What role does `form_for` play in helping us create our forms?
form_for is erb that allows us to code forms more easily and translates to html for us

10. How does `form_for` know where to submit the user's input?
you explicitly pass in parameters of the model

11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for @horses do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>
<%= f.submit %>
<% end %>

12. Why do we want to validate our models?
if models don't behave as intended, the database will not be built properly.

13. What are the steps of the DNS lookup?


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
Horse.move.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
!!furniture[:table[:height]]

16. What is inheritance?
gives sub classes methods and instance variables of super classes.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
