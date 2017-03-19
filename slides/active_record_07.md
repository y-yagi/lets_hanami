#### [PostgreSQL & MySQL: Use big integer as primary key type for new tables](https://github.com/rails/rails/commit/d7f55e987849c5a17f9d3152abd4fbacac08a509)

* 新規に作成するテーブルのprimary keyに、PostgreSQLは"bigserial"を、MySQLでは"BIGINT(8) UNSIGNED"をそれぞれ使用するようになった
* 型を変更した事によるパフォーマンスの影響は無い為との事
  * 参考：["Postgres reminder: train yourself to use BIGSERIAL, and never SERIAL…"](https://twitter.com/pvh/status/730141012048281600)
* 合わせて読みたい： [Restore the behaviour of the compatibility layer for integer\-like PKs](https://github.com/rails/rails/pull/27389)
