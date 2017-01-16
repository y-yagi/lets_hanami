## 性能測定

* 思ってたよりも性能差がでたので、同じ内容をPostgreSQLでも実施
* PostgreSQLにしたのは[sequel_pg](https://github.com/jeremyevans/sequel_pg)というpgのSELECTをCで実装したgemがある為
  * PostgreSQLには別途[doc](https://github.com/jeremyevans/sequel/blob/master/doc/postgresql.rdoc)もあり、対応が厚い
  * [Sequel PostgreSQL Triggers](https://github.com/jeremyevans/sequel_postgresql_triggers)何かもある
* PostgreSQLのバージョンは9.4.5
