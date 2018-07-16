## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new project_name
2. What do Models generally inherit from in rails?
  ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
  ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horses only: :new
5. What rake task is useful when looking at routes, and what information does it give you?
  rails routes, shows all routes your resources have given
6. What is an example of a route helper? When would you use them?
  Ex: new_song_path, edit_song_path, song_path(song), songs_path
  These helpers tell the controller which page to visit
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  There is no difference, both will return the same page, the `_url` request will be longer
8. What are strong params and why are they necessary?
  Strong params keep information hidden until certain requirements are met, such as white listing
9. What role does `form_for` play in helping us create our forms?
  It is the name of the form to make a form, like a div or p tag.
10. How does `form_for` know where to submit the user's input?
  Controller contains this information
11. Create a form using a `form_for` helper to create a new `Horse`.
  <%= form_for @horse do |f| %>
    <%= f.string :name %>
    <%= f.string :breed %>
    <%= f.string :color %>
    <%= f.string :height %>
  <% end %>


12. Why do we want to validate our models?
  AAAWTF
13. What are the steps of the DNS lookup?
  1. Browser queries client cache for server destination
  2. If internal cache does not know, next it queries the Root servers
  3. If the Root does not know, next it queries the Top Level Domain (TLD) servers
  4. If TLD does not know, it queries the Authoratative Name Servers (ANS)
  5. ANS returns the IP needed for the browser to send a request to the proper website

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
horse.move.prance
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?
  'true' is inside the main hash, whereas '3' is inside the secondary hash located inside the main hash
16. What is inheritance?
  Inheritance allows one class to know all the methods another class has, thus allowing it to call those methods as if it were it's own, and not have to call the other class first

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
*** I was able to answer most questions independently, but utilized outside resources for a few ***
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
*** I feel comfortable with the content presented this week ***
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
