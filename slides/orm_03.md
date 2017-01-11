## CRUD

* READ

```ruby
Article.where('id = ?', 13).to_a
# => SELECT * FROM "articles" WHERE (id = 13)

Article[1]
# => SELECT * FROM "articles" WHERE "id" = 1

Article.with_pk!(1)
# => SELECT * FROM "articles" WHERE "id" = 1
# []と異なりレコードが見つからなかった場合exceptionをraiseする
```
