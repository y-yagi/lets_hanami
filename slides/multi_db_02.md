## 複数DB(余談)

* Rails 5.1.0で複数DB対応が入りますね
  * [new database\.yml format](https://github.com/rails/rails/pull/27611)

```
default: &default
  adapter: sqlite3
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  timeout: 5000

development:
  primary:
    <<: *default
    database: db/development.sqlite3
  readonly:
    <<: *default
    database: db/readonly.sqlite3
```

* establish_connectionに接続先名(e.g. primary, readonly)を指定出来るようになる
