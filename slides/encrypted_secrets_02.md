### [Encrypted secrets](https://github.com/rails/rails/pull/28038)

まず secrets:setup コマンドでセットアップ処理を行う

```
./bin/rails secrets:setup
Adding config/secrets.yml.key to store the encryption key: bf55aca3c137840f79e2c5d9a2dd6937

Save this in a password manager your team can access.

If you lose the key, no one, including you, can access any encrypted secrets.

      create  config/secrets.yml.key

Ignoring config/secrets.yml.key so it won't end up in Git history:

      append  .gitignore

Adding config/secrets.yml.enc to store secrets that needs to be encrypted.

      create  config/secrets.yml.enc

For now the file contains this but it's been encrypted with the generated key:

# See `secrets.yml` for tips on generating suitable keys.
# production:
#  external_api_key: 1466aac22e6a869134be3d09b9e89232fc2c2289…

You can edit encrypted secrets with `bin/rails secrets:edit`.
Add this to your config/environments/production.rb:
config.read_encrypted_secrets = true
```
