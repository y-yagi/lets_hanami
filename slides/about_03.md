## example

```ruby
require 'sequel'

DB = Sequel.sqlite # on memory DB

# create table
DB.create_table :items do
  primary_key :id
  String :name
  Float :price
end

class Item < Sequel::Model; end

# insert data to table
Item.insert(name: 'abc', price: rand * 100)
Item.insert(name: 'def', price: rand * 100)
Item.insert(name: 'ghi', price: rand * 100)

# Print out the number of records
puts "Item count: #{Item.count}"

# Print out the average price
puts "The average price is: #{Item.avg(:price)}"
```
