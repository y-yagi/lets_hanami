### Helpers

```erb
<%=
  form_for :book, routes.books_path do
    div class: 'input' do
      label      :title
      text_field :title
    end

    div class: 'input' do
      label      :author
      text_field :author
    end

    div class: 'controls' do
      submit 'Create Book'
    end
  end
%>
```
