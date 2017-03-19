### [Encrypted secrets](https://github.com/rails/rails/pull/28038)

秘密情報を編集する為には、 secrets:edit コマンドを使用する

```
EDITOR="vim" bin/rails secrets:edit
```

秘密情報はymlで書ける

```yml
# See `secrets.yml` for tips on generating suitable keys.
# production:
#  external_api_key: 1466aac22e6a869134be3d09b9e89232fc2c2289…
```
