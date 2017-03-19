### [Direct & resolved routes](https://github.com/rails/rails/pull/23138)

**resolve**


```ruby
Rails.application.routes.draw do
  resource :basket

  # オプションも渡せる
  resolve "Basket", anchor: "items" do |basket, options|
    [:basket, options]
  end
end
```

```ruby
# actionが`/basket#items`になる
<%= form_for @basket do |form| %>
  <!-- basket form -->
<% end %>
```
