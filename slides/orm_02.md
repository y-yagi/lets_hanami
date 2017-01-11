## CRUD

* CREATE

```ruby
Article.create(title: 'Happy New Year!', text: '新年のご挨拶的なやつ')
#=> #<Article @values={:id=>23, :title=>"Happy New Year!", :text=>"新年のご挨拶的なやつ", :created_at=>2017-01-08 15:40:46 +0900, :updated_at=>nil}>

Article.insert(title: 'Happy New Year!', text: '新年のご挨拶的なやつ')
#=> 24

# insertはmodelのvalidation, callback等が実行されない
```
