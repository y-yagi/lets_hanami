### [Encrypted secrets](https://github.com/rails/rails/pull/28038)

* secrets.yml.enc を読み込む為のkeyは secrets.yml.keyに定義する以外に、環境変数(`ENV["RAILS_MASTER_KEY"]`)に設定する事が出来る
* secrets.yml.encの読み込み処理は config.read_encrypted_secretsにtrueが設定されている時しか行われない
* read_encrypted_secrets は デフォルトはfalseなので、注意が必要
  * 正確には、新規に作成されたRailsアプリではproduction envのみtrueが設定されている
