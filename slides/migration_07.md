## Migrations

```ruby
Sequel.migration do
  transaction
  change do
    # ...
  end
end
```

逆にtransactionを明示的に使用したくない場合は、no_transactionオプションを指定する

```ruby
Sequel.migration do
  no_transaction
  change do
    # ...
  end
end
```
