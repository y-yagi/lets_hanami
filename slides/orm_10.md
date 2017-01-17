## Model Plugins

* 例えば、created_at / updated_atの自動更新がtimestamps pluginとして提供されている

```ruby
class Article < Sequel::Model
  plugin :timestamps
end
```

``` ruby
irb(main):029:0* a = Article.create(title: "a", text: "b")
# => #<Article @values={:id=>40, :title=>"a", :text=>"b", :active=>false, :created_at=>2017-01-09 12:51:08 +0900, :updated_at=>nil}>
irb(main):030:0> a.update(text: "update")
# => #<Article @values={:id=>40, :title=>"a", :text=>"update", :active=>false, :created_at=>2017-01-09 12:51:08 +0900, :updated_at=>2017-01-09 12:51:15 +0900}>
```
