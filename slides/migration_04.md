## Migrations

```
$ tree .
├── migrate
│   └── 001_create_articles.rb
```

上記のようなディレクトリ構成の場合

```
sequel sqlite://developement.db -m migrate
```

でmigrationが実行出来る("-m"オプションにはmigrationファイルがあるディレクトリを指定)。

<small>
が、ARにおける"db:rollback"相当の処理が無く、実際のアプリでmigrateを実行する場合は、SequelのAPIをラップしたrakeタスクを準備するのが良さそう(詳細は後述)。
</small>
