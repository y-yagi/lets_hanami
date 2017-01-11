## composite primary key

* composite primary keyも使える
  * primary_key メソッドに配列を指定すればOK

```ruby
# migration
Sequel.migration do
  transaction
  change do
    create_table(:artists) do
      String :name
      String :city
      primary_key [:name, :city]
    end
  end
end
```

```ruby
Artist.primary_key
# => [:name, :city]
```
