### Exposures

* Railsと違い、インスタンス変数を宣言しただけではviewでその変数を使用する事が出来ない
* viewで使いたい変数は、明示的に"expose"メソッドを使って宣言する必要がある

```ruby
# apps/web/controllers/dashboard/index.rb
module Web::Controllers::Dashboard
  class Index
    include Web::Action
    expose :greeting

    def call(params)
      @greeting = "Hello"
      @foo      = 23
    end
  end
end
```
* 上記例だと、"greeting"はviewから使えるが、"foo"はviewからは使えない
