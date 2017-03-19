#### [Add :default option to belongs\_to by georgeclaghorn](https://github.com/rails/rails/pull/28453)

* `belongs_to`メソッドにデフォルト値を設定する為の`default`オプションを追加

```ruby
belongs_to :person, default: -> { Current.person }
belongs_to :account, default: -> { person.account }
```
