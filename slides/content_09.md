### [#duplicable?](https://github.com/rails/rails/pull/27293)

* Ruby 2.3まではNumericやTrue、Falseはdup出来なかったのが、Ruby 2.4からは出来るようになりました
* Railsにはクラスがdup出来るかどうかをチェックするためのduplicable?というメソッドがあり、当然Ruby 2.3より前と以降で結果が変わるようになっています
* 因みにまだMethodクラスだけdupできません
