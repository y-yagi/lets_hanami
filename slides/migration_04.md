## Migrations

```ruby
Sequel.migration do
  change do
    create_table(:comments) do
      primary_key :id
      foreign_key(:article_id, :articles)
      String :commenter, null: false
      Text :body, null: false
      Bool :active, default: false
      DateTime :created_at
      DateTime :updated_at
    end

    alter_table(:comments) do
      add_full_text_index(:body)
    end
  end
end
```
