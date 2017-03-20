### [System tests](https://github.com/rails/rails/pull/26703)

* なお、System testsとの絡みで、テスト実行時にスレッド間で同じDB connectionを使うように対応されている
  * [Ensure test threads share a DB connection](https://github.com/rails/rails/pull/28083)
* 今の所、上記処理が動作するのはfixturesを使用している時だけ
