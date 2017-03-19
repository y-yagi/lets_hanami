### [Module\#delegate\_missing](https://github.com/rails/rails/pull/23930)

**after**

```ruby
class Partition
  delegate_missing_to :@events

  def initialize(first_event)
    @events = [ first_event ]
  end

  def people
    if @events.first.detail.people.any?
      @events.collect { |e| Array(e.detail.people) }.flatten.uniq
    else
      @events.collect(&:creator).uniq
    end
  end
end
```
