### Actions


* 普通にRubyのクラスとして扱われる為、コンストラクタを定義する事も出来る

```ruby
# apps/web/controllers/dashboard/index.rb
module Web::Controllers::Dashboard
  class Index
    include Web::Action

    def initialize(greeting: Greeting.new)
      @greeting = greeting
    end

    def call(params)
      self.body = @greeting.message
    end
  end
end
```
