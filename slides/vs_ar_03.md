## 性能測定

```ruby
require "sequel"
require "active_record"
require "benchmark/ips"

ar_db = "ar.db"
sequel_db = "sequel.db"

File.delete(ar_db) rescue nil
File.delete(sequel_db) rescue nil

ActiveRecord::Base.establish_connection(adapter: "sqlite3", database: ar_db)
ActiveRecord::Schema.define do
  create_table :posts, force: true do |t|
    t.string :name
  end

  create_table :comments, force: true do |t|
    t.integer :post_id
  end
end

class ArPost < ActiveRecord::Base
  self.table_name = "posts"
  has_many :comments
end

class ArComment < ActiveRecord::Base
  self.table_name = "comments"
  belongs_to :post
end

DB = Sequel.connect("sqlite://#{sequel_db}")

DB.create_table :posts do
  primary_key :id
  String :name
end

DB.create_table :comments do
  primary_key :id
  Integer :post_id
end

class SequelPost < Sequel::Model(:posts)
  one_to_many :comments
end

class SequelComment < Sequel::Model(:comments)
  many_to_one :post
end

Benchmark.ips do |x|
  x.report("ar_insert") { ArPost.create(name: "dummy") }
  x.report("sequle_insert") { SequelPost.create(name: "dummy") }
  x.compare!
end

100.times { |i| ArPost.create(name: "dummy#{i}") }
100.times { |i| SequelPost.create(name: "dummy#{i}") }

Benchmark.ips do |x|
  x.report("ar_select") {  ArPost.all.each{} }
  x.report("sequel_select") { SequelPost.each{} }
  x.compare!
end
```
