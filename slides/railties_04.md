#### [Track the version\-compatible config settings inside railties](https://github.com/rails/rails/pull/28469)

* 新規config、かつ、非互換になる値の設定をrailtiesの中で行うようになった
  * Rails 5.0にあったnew_framework_defaults.rbというファイルで行っていた内容
* rails newで新規に作成したアプリではデフォルトで新しい値が設定されるようになっている
  * なお、自動で上記値の読み込みは行わない。load_defaultsメソッドを呼び出す必要がある。
* app:updateを実行した場合は、古い値が定義されているconfigファイルが生成されるようになっている
