#### [Add retry\_on/discard\_on for better exception handling](https://github.com/rails/rails/pull/25991)

Job実行中にexceptionが発生した場合に、処理をリトライ、又は破棄する為のActiveJob::Base.retry_on、ActiveJob::Base.discard_onメソッドが追加された
