### [BigDecimal - inconsistency with other numeric classes](https://github.com/rails/rails/commit/b87619f94550ad37a5a4825b0c2c1acdb96b5f6e)

* BigDecimal 1.3.0から、コンストラクタの引数に不正な値(文字列とか)を指定するとエラーになるようになりました

```ruby
# ruby 2.3
BigDecimal('invalid value') # => #<BigDecimal:7fe6f9a6a058,'0.0',9(9)>

# ruby 2.4
BigDecimal('invalid value') # => ArgumentError: invalid value for BigDecimal(): "invalid value"
```

* Railsではテストの修正だけ
