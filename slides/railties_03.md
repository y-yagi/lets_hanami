#### [Add config.assets.quiet = true as default value](https://github.com/rails/rails/commit/7c6c00e91f62fd25b6b670b40ee4c030fd429c3d)

* development envでは、デフォルトでassetのrequestsについてログ出力しないようになった
  * ようはquiet_assets
* Rails 5.0でも使えるが、5.1ではデフォルトでtrueになった
