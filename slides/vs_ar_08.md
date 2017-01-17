## オブジェクト生成数(PostgreSQL)

```ruby
ObjectSpace::AllocationTracer.trace { SequelPost.all.each{} }
p allocated: ObjectSpace::AllocationTracer.allocated_count_table
# => {:allocated=>{:T_NONE=>0, :T_OBJECT=>100, :T_CLASS=>0, :T_MODULE=>0, :T_FLOAT=>0, :T_STRING=>104, :T_REGEXP=>0, :T_ARRAY=>4, :T_HASH=>100, :T_STRUCT=>0, :T_BIGNUM=>0, :T_FILE=>0, :T_DATA=>7, :T_MATCH=>0, :T_COMPLEX=>0, :T_RATIONAL=>0, :unknown=>0, :T_NIL=>0, :T_TRUE=>0, :T_FALSE=>0, :T_SYMBOL=>0, :T_FIXNUM=>0, :T_UNDEF=>0, :T_IMEMO=>11, :T_NODE=>0, :T_ICLASS=>0, :T_ZOMBIE=>0}}


ObjectSpace::AllocationTracer.trace { ArPost.all.each{} }
p allocated: ObjectSpace::AllocationTracer.allocated_count_table
# => {:allocated=>{:T_NONE=>0, :T_OBJECT=>309, :T_CLASS=>3, :T_MODULE=>3, :T_FLOAT=>0, :T_STRING=>276, :T_REGEXP=>0, :T_ARRAY=>177, :T_HASH=>613, :T_STRUCT=>1, :T_BIGNUM=>0, :T_FILE=>1, :T_DATA=>15, :T_MATCH=>0, :T_COMPLEX=>0, :T_RATIONAL=>0, :unknown=>0, :T_NIL=>0, :T_TRUE=>0, :T_FALSE=>0, :T_SYMBOL=>0, :T_FIXNUM=>0, :T_UNDEF=>0, :T_IMEMO=>44, :T_NODE=>169, :T_ICLASS=>0, :T_ZOMBIE=>0}}
```

