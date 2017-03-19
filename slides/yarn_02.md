### [Yarn Support](https://github.com/rails/rails/pull/26836)

* bin/yarn の中身はこんな感じ

```ruby
#!/usr/bin/env ruby
VENDOR_PATH = File.expand_path('..', __dir__)
Dir.chdir(VENDOR_PATH) do
  begin
    exec "yarnpkg #{ARGV.join(" ")}"
  rescue Errno::ENOENT
    puts "Yarn executable was not detected in the system."
    puts "Download Yarn at https://yarnpkg.com/en/docs/install"
  end
end
```

* 一時node_modulesがvendor配下に置かれた時期もあったが、最終的にはRails root配下に置かれるようになっている
