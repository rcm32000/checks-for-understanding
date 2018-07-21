## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A cookie is a small package under 40kB is size, that holds information on a client's computer pertinent to the website that gave the cookie.
2. What’s the difference between a session and a cookie?
  A session is on the server side, while a cookie is all on the client side
3. What’s a flash and when do you want to use flashes?
  Flashes are used to say when something happened either successfully or unsuccessfully
4. Why do people say “HTTP is stateless”?
5. What’s authentication? Explain.
  Authentication is basically a digital form of identification, identifying the user
6. What’s the difference between authentication and authorization?
  Authentication is WHO you are, Authorization is WHAT you are allowed to see and do
7. What’s a before filter?
  Before filter is used when we want to check for a condition prior to running a controller
8. How do we keep track of a user once they’ve logged in?
  Sessions can be used to keep tracked of both a guest and registered user
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  Namespace - Nested resource depends on it, though it is not it's own entity
  Nested - Belongs to another class
  Nested deals with two tables, while namespace is for a table dependent on a temporary object
10. At a high level, what tools can you use to implement authorization? How would you use them?
  Use role to set authorization levels, and enum to check what level a user is
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  - Enum allows for a variable name to be stored as an integer
  - Enum must be added to model and define names that can be queried
12. What are some strategies you can use to keep your views DRY?


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
  Define incoming data as a float in the migration file prior to running rake db:migrate


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
*** I was able to answer most questions independently, but utilized outside resources for a few ***
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
*** I feel overwhelmed by the content presented this week ***
* I feel quite lost by the content presented this week
