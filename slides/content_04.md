### [Regexp#match?](https://github.com/rails/rails/commit/575dbeeefcaafeb566afc07cdd8b55603b698d9f)

* Ruby 2.4で正規表現にマッチしたかどうかチェックする為のRegexp#match?メソッドが追加されました
* Regexp#matchより高速なので、#matchでチェックしていた箇所を#match?を使うようrails内部でも書き直しが行われました
* となると、当然Ruby 2.3以下でどうするか、という問題が発生するのですが、Ruby 2.3でもRegexp#match?が使えるよう、ASにメソッドが追加されています
