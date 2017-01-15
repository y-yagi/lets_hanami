## CRUD

* UPDATE

```ruby
Article.where('id = ?', 13).update(title: '正月休みは終わってしまったのだ…')
```

* DELETE

```ruby
Article.exclude(active: true).delete
# => DELETE FROM "articles" WHERE ("active" IS NOT TRUE)

Article.dataset.delete
# => DELETE FROM "articles"
```
