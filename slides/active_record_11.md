#### [Virtual/generated column support for MySQL 5.7.5+ and MariaDB 5.2.0+.](https://github.com/rails/rails/pull/22589)

* migrationでMySQLのgenerated columns、及び、MariaDBのvirtual columnsを使用出来るよう対応
  * virtualメソッドで定義出来るようになっている

```ruby
create_table :generated_columns do |t|
  t.string  :name
  t.virtual :upper_name,  type: :string,  as: "UPPER(name)"
  t.virtual :name_length, type: :integer, as: "LENGTH(name)", stored: true
  t.index :name_length  # May be indexed, too!
end
```
