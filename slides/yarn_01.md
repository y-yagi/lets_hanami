### [Yarn Support](https://github.com/rails/rails/pull/26836)

* 下記対応が行われている
  * bin/yarn stubの追加
  * assets path にnode_modulesを追加
  * assets:precompile task 実行前にyarn installを実行するよう対応
* bin/yarn stub及び assets pathの追加はrails new時に追加・設定されるので、既存のアプリを更新する場合はapp:update task等により追加作業が必要
