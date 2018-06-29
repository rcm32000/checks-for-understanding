## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  DELETE  - Delete Selected Entry
  GET     - Read Selected Entry
  PATCH   - Change Portions of Selected Entry
  POST    - Create New Entry
  PUT     - Update Selected Entry
2. What is Sinatra?
  Web framework similar to Ruby on Rails
4. What is MVC?
  Model
  View
  Controller
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  Naming conventions exist not only to make code maintainable, and easy to read, but also certain conventions will break the code if not followed.
6. What types of variables are accessible in our view templates without explicitly passing them?
  Attributes (ex: name, id, age, description, etc)
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  Don't understand the question.  Am I modifying the code as well as showing what would go in the index? Here is my guess:
  <p>Horse Total: <%= horse.total_count %></p>
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  Are we filling out a form? Are we visiting single horse's page? Guess:
  <p>Name: <%= horse.name %></p>
9. What's the purpose of ERB?
  ERB is Embeded RuBy, a template for Ruby, allowing Ruby code to be added directly to plain text docs.
10. Why do I need a development AND test database?
  Testing will add/subtract data, which would corrupt actual database otherwise.
11. What is CRUD and why is it important?
  Create/Read/Update/Delete is the framework for basic commands with ActiveRecord in Sinatra, no need to write any of the listed commands.
12. What does HTTP stand for?
  HyperText Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  Instance Variable - Easier to read
  Scope - Can mix with other scopes
14. What's an ORM?
  Object Relational Mapping
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
17. What's a migration?
  A way to alter database easily using Ruby DSL.
18. When you create a migration, does it automatically modify your database?
  No it does not.
19. How does a model relate to a database?
  Model contains commands for the database, as well as acting as the go between for the Controller and the Database.
20. What is the difference between `#new` and `#create`?
  #new creates a new instance but does not save it
  #create creates a new instance and saves it

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?

  def from_csv(csv)
    films = CSV.read(csv, headers: true)
    attributes_list = (0..(films.count - 1)).to_a.map do |index|
      set_film_hash(films, index)
    end
    build_films_hash(attributes_list)
  end

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?
  activities[:hiking][:supplies] << 'granola bars'
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Abstraction   - Idea of Object Oriented Programming, to simplify complex problems
Polymorphism  - One method able to different things depending on data
Encapsulation - Keeping classes separate
Inheritance   - Allow one class to use another's methods


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

[{"* I was able to answer most questions independently, but utilized outside resources for a few"}]

* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week

[{"* I feel comfortable with the content presented this week"}]

* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
