#### [Add retry\_on/discard\_on for better exception handling](https://github.com/rails/rails/pull/25991)

* retry処理はRubyレベルで処理を行っており、adapterのメソッドは使用していない
* そのため、adapter側で提供されているretry用の処理に影響が出ないので注意が必要
  * Sidekiq UIのretry jobの一覧に表示されない、等
  * 参考： https://github.com/rails/rails/issues/28347
