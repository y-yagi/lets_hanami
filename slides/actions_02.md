### Actions

* Railsと異なり、1つのクラスに1つのアクションを定義する
* `index`アクションを定義する場合

```ruby
# apps/web/controllers/dashboard/index.rb
module Web::Controllers::Dashboard
  class Index
    include Web::Action

    def call(params)
      self.body = 'OK'
    end
  end
end
```

* 必要なのは、"Action" moduleのincludeと、"call"メソッドを定義する事だけ
* `view`の定義はViewクラスで行う(後述)
