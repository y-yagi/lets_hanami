#### [Remove the SchemaDumper options and change the default behavior](https://github.com/rails/rails/commit/df84e9867219e9311aef6f4efd5dd9ec675bee5c)

```ruby
create_table "address", force: :cascade do |t|
  t.string "zipcode",           limit: 5
  t.string "extra_information", limit: 255
end
```

となっていたのが

```ruby
create_table "address", force: :cascade do |t|
  t.string "zipcode", limit: 5
  t.string "extra_information", limit: 255
end
```
となります

