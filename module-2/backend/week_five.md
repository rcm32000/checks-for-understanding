### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  flash[:type_of_message] = 'Message'
2. Where is cart information/temporary information usually stored?
  Session
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  Database has to update every time a change is made, possible to lose database records
4. What is the purpose of the asset pipeline?
  Streamline loading performance of a website
5. Why do we precompile our assets?
  So the page has everything cached and ready to load ahead of time.
6. What do each of the following tags do?
```ruby
<%= stylesheet_link_tag "application" %>
  Concatenate CSS Files
<%= javascript_include_tag "application" %>
  Minify JavaScript Files
<%= image_tag "rails.png" %>
  Fingerprinting Images
```
7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  What it's purpose is, how to install/use it
  Improvements documented to show when and how, proving willingness to keep it up to date
8. What are the top four accessibility issues that we as developers should be aware of?

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  Callback
  Model
10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
  Main difference is scopes are very easy to chain together

### Review Questions:  
12. Given the following hash:  
```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```
  12a. How would you add item with id of 48 with a quantity of 4?
    cart['48'] = 4
  12b. How would you increase the quantity of item 29?
    cart['29'] = new_value
  12c. How would you find out how many items your user is thinking about purchasing?   
    cart.inject(&:+)
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  "(630) 854-5483".gsub(/['-',' ']/, '.') = "630.854.5483"

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
*** I was able to answer a few questions independently, but relied heavily on outside resources ***

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
*** I feel overwhelmed by the content presented this week ***
* I feel quite lost by the content presented this week
