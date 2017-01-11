## Migrations

* 外部キー設定(foreign_key)、CHECK制約(check)、VIEW作成(create_view)、や複合主キーの設定(e.g. "add_primary_key [:album_id, :artist_id]")用のメソッドも提供されている
  * create_viewに"materialized"オプションを指定する事でマテビューも作れる
* 大抵の事はRubyレベルで出来るようになっている
