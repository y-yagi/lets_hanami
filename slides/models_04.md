### Models

"book" に対するCRUDは"BookRepository"を経由して行う

```
repository = BookRepository.new
# => #<BookRepository relations=[:books]>

book = repository.create(title: "Hanami", author: "Luca Guidi")
# => #<Book:0x0056004d6addc8 @attributes={:id=>4, :title=>"Hanami", :author=>"Luca Guidi", :created_at=>2017-04-01 23:54:21 UTC, :updated_at=>2017-04-01 23:54:21 UTC}>

book = repository.find(book.id)
# => #<Book:0x0056004d6a3c10 @attributes={:id=>4, :title=>"Hanami", :author=>"Luca Guidi", :created_at=>2017-04-01 23:54:21 UTC, :updated_at=>2017-04-01 23:54:21 UTC}>

book = repository.update(book.id, title: "Hanami Book")
# => #<Book:0x0056004d67ef50 @attributes={:id=>4, :title=>"Hanami Book", :author=>"Luca Guidi", :created_at=>2017-04-01 23:54:21 UTC, :updated_at=>2017-04-01 23:54:31 UTC}>

repository.all
# => [#<Book:0x0056004d66b9a0 @attributes={:id=>1, :title=>"TDD", :author=>"Kent Beck", :created_at=>2017-03-26 01:48:15 UTC, :updated_at=>2017-03-26 01:48:15 UTC}>, #<Book:0x0056004d66ac30 @attributes={:id=>2, :title=>"3", :author=>"1", :created_at=>2017-03-26 01:54:19 UTC, :updated_at=>2017-03-26 01:54:19 UTC}>, #<Book:0x0056004d669ec0 @attributes={:id=>4, :title=>"Hanami Book", :author=>"Luca Guidi", :created_at=>2017-04-01 23:54:21 UTC, :updated_at=>2017-04-01 23:54:31 UTC}>]
```

戻り値は"Book"クラスのインスタンス
