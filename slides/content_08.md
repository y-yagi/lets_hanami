### [Hash#compact(!)](https://github.com/rails/rails/commit/3cc30db12ca4b92d6c46a2fd28b2622c7ba4fe42)

* Ruby 2.4でHash#compact(!)が追加されました
* 元々ASで同様のメソッドが定義されていましたが、Ruby 2.4で追加されたcompactは挙動が同じだった為、Ruby本体でHash#compactが定義されていれば、ASでは定義しないよう対応が入りました
* これもHashWithIndifferentAccessに影響が(ry
