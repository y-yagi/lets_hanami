#### [Delegate to scope rather than merge! for collection proxy ](https://github.com/rails/rails/commit/eb41ac40cb05874863ce24f0c2547b191db1211c)

* collection proxyを生成する際に必ずassocation.scopeの結果をmergeしていたのを、必要に応じてscope`(assocation.scope)にメソッド呼び出しをdelegateするようにして、不要な場合はassocationのscope呼び出し、及びmerge処理を行わないよう修正
* これにより、has_manyが大分高速化(単純なケースだと170倍速くなっているとのこと)
