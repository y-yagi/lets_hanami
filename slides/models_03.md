### Models

 "book"というmodelがあった場合

```ruby
# db/migrations/20170326014641_create_books.rb
Hanami::Model.migration do
  change do
    create_table :books do
      primary_key :id

      column :title,  String, null: false
      column :author, String, null: false

      column :created_at, DateTime, null: false
      column :updated_at, DateTime, null: false
    end
  end
end

# lib/bookshelf/entities/book.rb
class Book < Hanami::Entity
end

# lib/bookshelf/repositories/book_repository.rb
class BookRepository < Hanami::Repository
end
```
