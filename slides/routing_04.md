### Routing

* Routingを取得する為のヘルパーメソッドもある

```ruby
<%= routes.path(:greeting) %>
<%= routes.url(:greeting) %>
```

または

```
<%= routes.greeting_path %>
<%= routes.greeting_url %>
```
