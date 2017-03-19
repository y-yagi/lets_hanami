#### [Deprecate the behavior of AR::Dirty inside of after\_\(create\|update\|save\) callbacks](https://github.com/rails/rails/pull/25337)

* after callbackの中でdirtyメソッドを呼んだ時の挙動がユーザが想定している挙動と異なる
  * Model.after_save { puts changed? }; model.save が model.save; puts model.changed? と同じ挙動になる事を期待している事が多いようだが、実際は違う
* ユーザの混乱の元になる(この絡みのissueが多い)、という事でdeprecateにしたとのことです
