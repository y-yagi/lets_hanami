
### Template

* デフォルトではクラス名に指定された名前のファイルを使用する
 * "Web::Views::Dashboard::New" というクラス名だった場合、デフォルトは"web/templates/dashboard/new.html.erb"
* 任意のテンプレートを使用したい場合は、"template"メソッドで指定する

```ruby
module Web::Views::Books
  class Create
    include Web::View
    template 'books/new'
  end
end
```

