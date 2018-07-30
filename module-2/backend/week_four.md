## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
An HTTP cookie is a small piece of data sent from a website and stored on the user's computer by the user's web browser while the user is browsing.  The state is saved in a cookie and sent with every request because HTTP doesn't remember state.

2. What’s the difference between a session and a cookie?
Session is stored on the server. Cookies are stored on the computer and sent with every request.  Cookies have an ID that points to the session on the server which holds the data used.

3. What’s a flash and when do you want to use flashes?
The flash provides a way to pass temporary primitive-types (String, Array, Hash) between actions. Anything you place in the flash will be exposed to the very next action and then cleared out.

4. Why do people say “HTTP is stateless”?
Every request/response cycle is like a brand new cycle that doesn't hold information.  If information needs to be save from one cycle to the next, it needs to be sent every time.  

5. What’s authentication? Explain.
Authentication is the process for determining who you are as a client.

6. What’s the difference between authentication and authorization?
Authorization is the process of giving permissions to do certain actions or browse certain parts of a site.

7. What’s a before filter?
A before filter designates a method that is run before any (or designated) controller action.

8. How do we keep track of a user once they’ve logged in?
Session data is used to track whether a user is logged in.

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Namespacing designates controllers or certain controller actions to certain routes.  Nesting resources daisy chains routes so that one is required before the other.

10. At a high level, what tools can you use to implement authorization? How would you use them?
Bcrypt combined with session data can store and require hashed passwords to authorize users.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
Enums enumerate named roles with integers.  Integers are stored in the database, taking up less space and being searched faster, and point to a role name that can be used to describe the role.

12. What are some strategies you can use to keep your views DRY?



### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
ary = Array.map do |elem|
  elem[:holiday][:name]
end

ary.sort.each do |elem|
  puts elem
end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?


### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel comfortable with the content presented this week
