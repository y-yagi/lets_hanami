### [Module\#delegate\_missing](https://github.com/rails/rails/pull/23930)

**before**

```ruby
class Partition
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

  private
    def respond_to_missing?(name, include_private = false)
      @events.respond_to?(name, include_private)
    end

    def method_missing(method, *args, &block)
      @events.send(method, *args, &block)
    end
end
```
