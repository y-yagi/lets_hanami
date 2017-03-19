#### [Deprecate the behavior of AR::Dirty inside of after\_\(create\|update\|save\) callbacks](https://github.com/rails/rails/pull/25337)

```ruby
class User < ApplicationRecord
  after_save :post_processing

  def post_processing
    puts changed?
  end
end
```

```
User.create!
# => DEPRECATION WARNING: The behavior of `changed?` inside of after callbacks will be changing in the next version of Rails. The new return value will reflect the behavior of calling the method after `save` returned (e.g. the opposite of what it returns now). To maintain the current behavior, use `saved_changes?` instead. (called from post_processing at /home/yaginuma/program/rails/master/app/models/user.rb:5)
# => DEPRECATION WARNING: The behavior of `changed_attributes` inside of after callbacks will be changing in the next version of Rails. The new return value will reflect the behavior of calling the method after `save` returned (e.g. the opposite of what it returns now). To maintain the current behavior, use `saved_changes.transform_values(&:first)` instead. (called from post_processing at /home/yaginuma/program/rails/master/app/models/user.rb:5)
```
