### Associations

```ruby
# db/migrations/20170402002401_create_users.rb
Hanami::Model.migration do
  change do
    create_table :users do
      primary_key :id

      column :name,       String,   null: false
      column :created_at, DateTime, null: false
      column :updated_at, DateTime, null: false
    end
  end
end

# db/migrations/20170402002500_create_todos.rb
Hanami::Model.migration do
  change do
    create_table :todos do
      primary_key :id
      foreign_key :user_id, :users, on_delete: :cascade, null: false

      column :title,      String,   null: false
      column :created_at, DateTime, null: false
      column :updated_at, DateTime, null: false
    end
  end
end
```

