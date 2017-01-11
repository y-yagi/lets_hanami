## Migrations

reversible migrationsの場合、"change"メソッドが使える

```ruby
Sequel.migration do
  change do
    create_table(:articles) do
      primary_key :id
      String :title, null: false
      String :text, null: false
    end
  end
end
```
