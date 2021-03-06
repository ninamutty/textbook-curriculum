# Advanced Active Record Validations

## Learning Goals
- Identify areas where standard rails validators would not cover all of your validation needs
- Custom validations
- Custom validation methods

### Custom Validations

Rails provides a number of validators for you to utilize, but there may be cases where you have your own validation that you'd like to utilize.

Rails allows you to create two types of custom validators.

Custom validators are classes that you create that extend the `ActiveModel::Validator` class. This class must implement a `validate` method which will perform the validation. The result of the validation method should be an updated errors hash if the validation has not passed.

Within the model class where you would like to use the new validation, you use `validates_with` to specify the custom validator class that you want to use.

These new validator classes should be placed in the `app/validators` folder so that Rails can load them automatically for your use.


```ruby

     # in app/validators/MyValidator.rb
   class MyValidator < ActiveModel::Validator
    def validate(task)
      unless task.due_date >= Date.now
        record.errors[:due_date] << 'The task must be due at a future date!'
      end
    end
  end
 
  # in app/models/Task.rb
  class Task < ActiveRecord::Base
    validate :name, presence: :true
    validates_with MyValidator
  end
```

### Custom methods
Custom validation methods are different than custom validators because they exist within the model class itself. The result of the validation method should be an updated errors hash if the validation has not passed (same as the custom validator class).

Within the model class you use `validates` to specify the custom validation method that you want to use.

Since these custom methods exist within the model class itself, there is no additional work that needs to be done to integrate the custom methods with the model.

This example is from a MediaRanker Item model.

```ruby
class Item < ActiveRecord::Base

  # Defining Custom validator method
  validate :type_must_be_limited

  # A MediaRanker Item can only be a book, movie or album.
  def type_must_be_limited
    if kind != "Movie" && kind != "Book" && kind != "Album"
      errors.add(:kind, "Must be a Book, Movie or Album")
    end
  end

end
```

### Conditional Validations
TODO

## Resources
[Custom Validations](http://guides.rubyonrails.org/active_record_validations.html#performing-custom-validations)  
[Conditional Validations](http://guides.rubyonrails.org/active_record_validations.html#conditional-validation)  
