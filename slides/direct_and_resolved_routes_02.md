### [Direct & resolved routes](https://github.com/rails/rails/pull/23138)

**direct**

```ruby
Rails.application.routes.draw do
  direct :homepage do
    "http://www.rubyonrails.org"
  end

  direct :commentable do |model|
    [ model, anchor: model.id ]
  end

  direct :main do
    { controller: "page", action: "index" }
  end

  direct :browse, page: 1, size: 10 do |options|
    [ :products, options.merge(params.permit(:page, :size).to_h.symbolize_keys) ]
  end
end
```
