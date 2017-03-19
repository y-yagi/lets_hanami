### [Regexp#match?](https://github.com/rails/rails/commit/575dbeeefcaafeb566afc07cdd8b55603b698d9f)

* Regexp#match? を追加
  * Ruby 2.4で本体に追加されたのと同じAPI
* Rails内部でRuby 2.2 / 2.3でもRegexp#match?を使用出来るようにする為にメソッドを追加
