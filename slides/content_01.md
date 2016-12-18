### [Support for unified Integer class in Ruby 2.4](https://github.com/rails/rails/commit/89e2f7e722e06f900bdb1c14db33073c90d7cdea)

* Fixnum と BignumがIntegerに統合された件の対応
* 基本的にはIntegerを使うように修正されていますが、下位互換の為に一部Fixnum、Bignumが残っています
