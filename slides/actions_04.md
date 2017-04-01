### Params


* Rails同様、params変数を操作すればOK

```ruby
module Web::Controllers::Dashboard
  class Index
    include Web::Action

    def call(params)
      self.body = "Query string: #{ params[:q] }"
    end
  end
end
```
