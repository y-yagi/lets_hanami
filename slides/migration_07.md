## Migrations

* Rails同様、migrationの実行履歴はtableで管理される
  * "schema_info" tableにversionが記録される
* migrationファイルのフォーマットは"IntegerMigrator"と"TimestampMigrator"の2タイプがサポートされている
