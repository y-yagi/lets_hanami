#### [jQuery no longer a default dependency](https://github.com/rails/rails/pull/27113)

* 因みにrails-ujsは色々議論された結果、Railsリポジトリの中にソースが含まれた
  * Action Viewの中にいる
  * [rails/actionview/app/assets/javascripts · rails/rails](https://github.com/rails/rails/tree/master/actionview/app/assets/javascripts)
* そのため、rails-ujsを使用するのに別途インストール等は不要
* PRの送り先は rails/railsなので注意
  * [rails/rails\-ujs](https://github.com/rails/rails-ujs)は消えるはず。多分。
