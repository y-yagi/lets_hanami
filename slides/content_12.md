### [parentheses after method name](https://github.com/rails/rails/commit/2f6105e49411e6c2a4603a7bf828d3fb4dfd0601)

* Ruby 2.4からメソッド名と引数の括弧の間にスペースがあるとwarningが出るようになりました

```ruby
def @cache.delete_entry (*args)

#=> test/caching_test.rb:986: warning: parentheses after method name is interpreted as
#=> test/caching_test.rb:986: warning: an argument list, not a decomposed argument
```

* テストの修正だけ
