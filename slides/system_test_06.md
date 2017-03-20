### [System tests](https://github.com/rails/rails/pull/26703)

* bin/rails test や bin/rake test ではデフォルトではSystem tests が実行されないのでちょっと注意が必要
  * System testsを行いたい場合は、bin/rails test:system タスクや、test runnerにsystemディレクトリを指定する必要がある
  * System testは遅いから通常のテストスイートと別buildにしたほうがよいから、とのこと
  * https://github.com/rails/rails/pull/28286#issuecomment-284507788
