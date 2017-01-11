## Associations

```ruby
class Article < Sequel::Model
  one_to_many :comments
end

class Comment < Sequel::Model
  many_to_one :article
end
```

```ruby
Article.first.comments
#=> [#<Comment @values={:id=>1, :article_id=>34, :commenter=>"userA", :body=>"really?", :created_at=>nil, :updated_at=>nil}>, #<Comment @values={:id=>2, :article_id=>34, :commenter=>"userB", :body=>"unfortually", :created_at=>nil, :updated_at=>nil}>]

Comment.first.article
#=> #<Article @values={:id=>34, :title=>"Happy New Year!", :text=>"新年のご挨拶的なやつ", :active=>false, :created_at=>2017-01-09 12:07:18 +0900, :updated_at=>nil}>
```
