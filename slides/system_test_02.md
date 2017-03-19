### [System tests](https://github.com/rails/rails/pull/26703)

```ruby
# test/application_system_test_case.rb
require "test_helper"

class ApplicationSystemTestCase < ActionDispatch::SystemTestCase
  driven_by :selenium, using: :chrome, screen_size: [1400, 1400]
end
```

```ruby
# test/system/todos_test.rb
require "application_system_test_case"

class TodosTest < ApplicationSystemTestCase
  # test "visiting the index" do
  #   visit todos_url
  #
  #   assert_selector "h1", text: "Todo"
  # end
end

```
