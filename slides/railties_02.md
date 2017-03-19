#### [Added a shared section to config/secrets\.yml](https://github.com/rails/rails/commit/e530534265d2c32b5c5f772e81cb9002dcf5e9cf)

* secrets.ymlに全ての環境で共通で使用出来るkeyを定義出来るようsharedセクションを追加

```
# Shared secrets are available across all environments.

shared:
  api_key: 123
```
