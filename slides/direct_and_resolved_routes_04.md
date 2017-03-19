### [Direct & resolved routes](https://github.com/rails/rails/pull/23138)

**resolve**


```ruby
Rails.application.routes.draw do
  resource :basket

  resolve "Basket" do
    [:basket]
  end
end
```

```ruby
# actionが`/baskets/:id` ではなく`/basket`になる
<%= form_for @basket do |form| %>
  <!-- basket form -->
<% end %>
```
