## transaction

* デフォルトのtransactionの設定はDBによって異なる
  * transactional DDL をサポートしているDB(e.g. PostgreSQL)ではデフォルトでmigrationの実行はtransaction内で行われる
  * transactional DDLをサポートしていないMySQLやsqliteではデフォルトではtransactionは使用されない。transactionを使用したい場合、明示的にオプションを指定する必要がある
