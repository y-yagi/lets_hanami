### [System tests](https://github.com/rails/rails/pull/26703)

* スクリーンショット取得処理は環境変数(RAILS_SYSTEM_TESTING_SCREENSHOT)により挙動が制御出来るようになっている
* 指定出来る値はinline(デフォルト。iTerm image protocol (http://iterm2.com/documentation-images.html)で表示。)、simple(スクリーンショットのファイルのパスだけ表示)、artifact(terminal artifact format (http://buildkite.github.io/terminal/inline-images/) で表示)の3つ
