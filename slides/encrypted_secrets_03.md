### [Encrypted secrets](https://github.com/rails/rails/pull/28038)

* secrets:setup コマンドでは secrets.yml.key と secrets.yml.enc という2つのファイルが生成される
* secrets.yml.enc が暗号化されたデータが格納されているファイル
* secrets.yml.key には secrets.yml.enc を暗号 / 復号処理に使用するkeyが格納されている
  * 当然keyは秘密情報になるので、デフォルトで gitignoreにsecrets.yml.keyが追加される
