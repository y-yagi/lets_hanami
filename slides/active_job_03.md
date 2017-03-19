#### [Add retry\_on/discard\_on for better exception handling](https://github.com/rails/rails/pull/25991)

```ruby
class RemoteServiceJob < ActiveJob::Base
  retry_on CustomAppException # デフォルトでは3秒waitし、5回再実行を行う
  retry_on AnotherCustomAppException, wait: ->(executions) { executions * 2 }
  retry_on ActiveRecord::StatementInvalid, wait: 5.seconds, attempts: 3
  retry_on Net::OpenTimeout, wait: :exponentially_longer, attempts: 10
  # `exponentially_longer`を指定するとjobが失敗する毎にwait時間が長くなる(最初は3s, 次は18s, 次は83s)
  # 計算式は (executions ** 4) + 2)

  discard_on ActiveJob::DeserializationError

  def perform(*args)
    # ...
  end
end
```

