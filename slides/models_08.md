### Associations

```ruby
class UserRepository < Hanami::Repository
  associations do
    has_many :todos
  end

  def create_with_todos(data)
    assoc(:todos).create(data)
  end

  def find_with_todos(id)
    aggregate(:todos).where(id: id).as(User).one
  end
end
```
