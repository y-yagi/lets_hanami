#### [Add ActiveRecord::Base\.connection\_pool\.stat](https://github.com/rails/rails/pull/26988)

* ActiveRecord::ConnectionAdapters::ConnectionPoolにconnection poolの状態を返す`stat`メソッドを追加

```ruby
ActiveRecord::Base.connection_pool.stat # => { size: 15, connections: 1, busy: 1, dead: 0, idle: 0, waiting: 0, checkout_timeout: 5 }
```
