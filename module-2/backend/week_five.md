### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
Include the flash message in the controller action that calls the show action.

2. Where is cart information/temporary information usually stored?
In session data and instance variables within classes.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
Carts shouldn't be saved in the db when a visitor isn't signed in.  We might want to persist cart info so a visitor can register or sign in to checkout.  We might also want to persist cart data for signed in users so they may come back and have their contents still in their cart.

4. What is the purpose of the asset pipeline?
The asset pipeline enables path helpers and erb tags to easily call assets.

5. Why do we precompile our assets?
Precompile converts rails to html, css, and javascript.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %> - this is erb shorthand for stylesheet html tag.
<%= javascript_include_tag "application" %> - this is erb shorthand for javascript html tag.
<%= image_tag "rails.png" %> - this is erb shorthand for image html tags.
```


7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
The purpose of the project, how to use it and install it, how to set up the dev environment.  Benefits include getting others to actually use it.

8. What are the top four accessibility issues that we as developers should be aware of?
I don't know.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
before_save is a callback.  This would be found in our models.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
helper_method :current_user

def current_user
  if session[:user_id]
    @current_user ||= User.find(session[:user_id])
  end
end

11. What is the difference between a scope and a class method?
Not much.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  my_hash[:cart]['48'] = 4
  12b. How would you increase the quantity of item 29?  my_hash[:cart]['29'] += x
  12c. How would you find out how many items your user is thinking about purchasing?   my_hash[:cart].values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
I don't know.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
number_to_phone(1235551234, delimiter: ".")

### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel comfortable with the content presented this week
