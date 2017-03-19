#### [Unification of form_for and form_tag into form_with](https://github.com/rails/rails/pull/26976)

form_for 的な使い方

```ruby
<%= form_with model: Post.new do |form| %>
  <%= form.text_field :title %>
<% end %>

# =>

<form action="/posts" method="post" data-remote="true">
  <input type="text" name="post[title]">
</form>
```
