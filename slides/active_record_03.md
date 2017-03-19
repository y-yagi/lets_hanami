#### [Deprecate the behavior of AR::Dirty inside of after\_\(create\|update\|save\) callbacks](https://github.com/rails/rails/pull/25337)

* after callbacks(after_create、after_update、after_save)の中で`ActiveRecord::Dirty`のメソッド(#previous_changes、#changed?)等を使うのがdeprecateになった
