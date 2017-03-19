#### [Add :skip_pipeline option to several asset tag helpers](https://github.com/rails/rails/pull/26226)

* 合わせて、helper methodに存在しないファイルを指定した場合にexceptionをraiseするかどうかの設定(config.assets.unknown_asset_fallback)を追加
  * 新規に作成するrailsアプリではfalse(exceptionをraiseする)になってる
  * 既存の挙動(exceptionをraiseしない)にしたい場合は、trueを指定すればOK
* 参考：[Deprecate asset fallback](https://github.com/rails/sprockets-rails/pull/375)
