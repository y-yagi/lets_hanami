### [Hash#transform_values(!)](https://github.com/rails/rails/commit/1167df3d11434de80d7e2533dbd1c1177e1805d1)

* Ruby 2.4でHash#transform_values(!)が追加されました
* 元々ASで同様のメソッドが定義されていましたが、Ruby 2.4で追加されたtransform_valuesは挙動が同じだった為、Ruby本体でHash#transform_valuesが定義されていれば、ASでは定義しないよう対応が入りました
* が、後でHashWithIndifferentAccessに影響がある事がわかり、別途HashWithIndifferentAccess#transform_valuesが追加されたりしたりもしました
