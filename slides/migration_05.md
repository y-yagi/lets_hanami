## Migrations

```
$ tree .
├── migrate
│   └── 001_create_articles.rb
│   └── 002_create_todos.rb
│   └── 003_add_status_to_articles.rb
```

上記のようなディレクトリ構成の場合

```
sequel sqlite://developement.db -m migrate
```

でmigrationが実行出来る("-m"オプションにはmigrationファイルがあるディレクトリを指定)。

<small>
が、ARにおける"db:rollback"相当の処理が無く、実際のアプリでmigrateを実行する場合は、SequelのAPIをラップしたrakeタスクを準備するのが良さそう
</small>
