#### [Unification of form_for and form_tag into form_with](https://github.com/rails/rails/pull/26976)

form_tag 的な使い方

```ruby
<%= form_with url: posts_path do |form| %>
  <%= form.text_field :title %>
<% end %>

# =>

<form action="/posts" method="post" data-remote="true">
  <input type="text" name="title">
</form>
```
