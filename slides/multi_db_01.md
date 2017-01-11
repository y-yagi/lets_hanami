## 複数DB

* デフォルトで複数DBのサポートがある

```ruby
require 'sequel'
require 'logger'
DB = Sequel.connect('postgres://localhost/sequel_example',
                    servers: { slave: { host: 'localhost', database: 'sequel_example_slave' } })

# default serverからデータ取得
puts Article.server(:default).all

# slaveからデータ取得
puts Article.server(:slave).all

# server名を指定しない場合はでdefaut serverからデータが取得される
puts Article.all
```
