## Associations

* Eager Loadも出来る
* メソッドが2つ(eager, eager_graph)ある(JOIN用とpreload用)

```ruby
Comment.all { |c| puts c.article }
# => SELECT * FROM "comments"
# => SELECT * FROM "articles" WHERE "id" = 34
# => SELECT * FROM "articles" WHERE "id" = 34
# => SELECT * FROM "articles" WHERE "id" = 34

Comment.eager(:article).all { |c| puts c.article }
# => SELECT * FROM "comments"
# => SELECT * FROM "articles" WHERE ("articles"."id" IN (34, 38))

Comment.eager_graph(:article).all { |c| puts c.article }
# => SELECT "comments"."id", "comments"."article_id", "comments"."commenter", "comments"."body", "comments"."created_at", "comments"."updated_at", "article"."id" AS "article_id_0", "article"."title", "article"."text", "article"."active", "article"."created_at" AS "article_created_at", "article"."updated_at" AS "article_updated_at" FROM "comments" LEFT OUTER JOIN "articles" AS "article" ON ("article"."id" = "comments"."article_id")
```

