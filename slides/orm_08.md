## Validations

* validation用のメソッドもある
* validation用のメソッドはcoreに含まれておらず、別途pluginを追加する必要がある

```ruby
class Album < Sequel::Model
  plugin :validation_helpers

  def validate
    super
    validates_presence [:name, :website]
    validates_unique :name
    validates_format /\Ahttps?:\/\//, :website, :message=>'is not a valid URL'
  end
end
```
