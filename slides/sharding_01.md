## Sharding

* デフォルトでShardingのサポートがある

```ruby
servers = {}
(('0'..'9').to_a + ('a'..'f').to_a).each do |hex|
  servers[hex.to_sym] = {:host=>"hash_host_#{hex}"}
end
DB = Sequel.connect('postgres://hash_host/hashes', :servers=>servers)
```

```ruby
class Rainbow < Sequel::Model(:hashes)
  plugin :sharding
end

Rainbow.server(:a).first.update(plaintext: 'VGM')
```
* sharding pluginはassociation取得時にインスタンスと同じshadeを使う、modelの保存時に同じshadeから値を返す、等の機能を提供している

