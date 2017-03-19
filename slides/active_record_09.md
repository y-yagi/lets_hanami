#### [Introduce new ActiveRecord transaction error classes](https://github.com/rails/rails/pull/25107)

* serialization failureになった場合 ActiveRecord::SerializationFailure が、deadlockになった場合 ActiveRecord::Deadlocked がraiseされるよう修正された
  * 上のPRではエラークラス名が DeadlockDetected になっているが、後から Deadlocked に変更されている
  * [The problem isn't the detection but the deadlock itself](https://github.com/rails/rails/pull/26059)

