## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is a program that allows us to interact with a database.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
.find
.all
.count
  If not defined, they are inherited through the ActiveRecord class.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4?
  Team.find(4)

Assuming your class only included the code from question 2, how could you find the owner of the same team?
  Team.find(4).owner_id

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Owner.find_by_team_id(4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
class Teacher
  has_many :students
end

class Student
  belongs_to :teacher
end

6. Define foreign key, primary key, and schema.
Foreign key = Column name/table key, that two tables share
Primary key = ID column of a table's main attribute
Schema = Blueprint for table creation

7. Describe the relationship between a foreign key on one table and a primary key on another table.
  Primary key of Students would be a foreign key in the Teachers table. We link tables by taking the primary key of one table, and making it a column/foreign key on another.

8. What are the parts of an HTTP response?
Get    = Read
Post   = Update part of the info
Put    = Update all info
Delete = Delete entry/info

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
  Created_at and Updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  Schools has_many :teachers, Teachers belongs_to :school
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
class School
  has_many :teachers
end

class Teacher
  belongs_to :school
end

6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
class Doctor
  has_many :patients
end

class Patient
  belongs_to :doctor
end

or

class Doctor
has_many :patients
end

class Patient
has_many :doctors
end


8. Describe and diagram the relationship between museums and original_paintings.
class Museum
  has_many :original_paintings
end

class OriginalPainting
  belongs_to :museum
end

9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* ***I was able to answer most questions independently, but utilized outside resources for a few***
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* ***I feel comfortable with the content presented this week***
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
