### [New syntax for tag helpers](https://github.com/rails/rails/pull/25543)

**before**

```ruby
tag(:br, nil, true)
content_tag(:div, content_tag(:p, "Hello world!"), class: "strong")

<%= content_tag :div, class: "strong" do -%>
  Hello world!
<% end -%>
```

**after**

```ruby
tag.br
tag.div tag.p("Hello world!"), class: "strong"

<%= tag.div class: "strong" do %>
  Hello world!
<% end %>
```
