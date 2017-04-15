### Associations

```ruby
repository = UserRepository.new
# => #<UserRepository relations=[:users :todos]>

repository.create_with_todos(name: "Alexandre Dumas", todos: [{title: "Create issue"}])
# => #<User:0x00564d5ec98900 @attributes={:id=>1, :name=>"Alexandre Dumas", :created_at=>2017-04-02 00:27:53 UTC, :updated_at=>2017-04-02 00:27:53 UTC, :todos=>[#<Todo:0x00564d5ec8b688 @attributes={:id=>1, :user_id=>1, :title=>"Create issue", :created_at=>2017-04-02 00:27:53 UTC, :updated_at=>2017-04-02 00:27:53 UTC}>]}>

user.todos
# => [#<Todo:0x00564d5ebd5fb8 @attributes={:id=>1, :user_id=>1, :title=>"Create issue", :created_at=>2017-04-02 00:27:53 UTC, :updated_at=>2017-04-02 00:27:53 UTC}>]

user = repository.find(user.id)
user.todos
# => nil

user = repository.find_with_todos(user.id)
user.todos
# => [#<Todo:0x00564d5ebd5fb8 @attributes={:id=>1, :user_id=>1, :title=>"Create issue", :created_at=>2017-04-02 00:27:53 UTC, :updated_at=>2017-04-02 00:27:53 UTC}>]
```
