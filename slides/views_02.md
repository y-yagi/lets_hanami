### Views

* Viewの定義はView Classで行う

```ruby
# apps/web/views/dashboard/index.rb
module Web::Views::Dashboard
  class Index
    include Web::View
  end
end
```
* クラス名にそのviewを使用するアクション名を指定する
* その為、アクション毎にClassが必要になる
