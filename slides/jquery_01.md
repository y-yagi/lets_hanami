#### [jQuery no longer a default dependency](https://github.com/rails/rails/pull/27113)

* 元々Railsはview helper用のJSの実装にjQueryを使っていた([jquery-rails](https://github.com/rails/jquery-rails))
* しかしもうjQueryを使う必要は無いだろう、という事で、jQueryを使わず、素のJSだけで実装するよう変更された
  * 変更後のライブラリ名はrails-ujs
* これによりデフォルトのスタックにはjQueryは含まれなくなったので、引き続きjQueryを使いたい場合は明示的に依存に追加する必要がある
  * 因みにjquery-rails自体は引き続き使用出来る(メンテもまだされる)
