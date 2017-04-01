### Views

* View Classとtemplateはコンテキストが一緒なので、View Classで定義したメソッドは、templateが呼び出す事が可能

```ruby
# apps/web/templates/dashboard/index.html.erb
<h1><%= title %></h1>
```

```
# apps/web/views/dashboard/index.rb
module Web::Views::Dashboard
  class Index
    include Web::View

    def title
      'Dashboard'
    end
  end
end
```
* 当然controllerで定義する事も可能だが、"expose"が必要 + 変数しか使えない
