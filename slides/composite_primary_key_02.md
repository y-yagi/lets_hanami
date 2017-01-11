## composite primary key

* associationも使える

```ruby
class Artist < Sequel::Model
  unrestrict_primary_key

  one_to_many :albums, key: [:artist_name, :artist_city]
end

class Album < Sequel::Model
  many_to_one :artist, key: [:artist_name, :artist_city]
end
```

```ruby
Artist.first.albums
# => [#<Album @values={:id=>2, :name=>"OFF THE LOCK", :artist_name=>"B'z", :artist_city=>"Tokyo", :release=>nil}>, #<Album @values={:id=>3, :name=>"BREAK THROUGH ", :artist_name=>"B'z", :artist_city=>"Tokyo", :release=>nil}>, #<Album @values={:id=>4, :name=>"RISKY", :artist_name=>"B'z", :artist_city=>"Tokyo", :release=>nil}>]

Album.first.artist
# => #<Artist @values={:name=>"B'z", :city=>"Tokyo"}
```

