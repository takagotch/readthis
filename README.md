### readthis
---

https://github.com/sorentwo/readthis

```
gem 'readthis'
gem 'hiredis'

```

```ruby
config.cache_store = :readthis_store, {
  expires_in: 2.weeks.to_i,
  namespace: 'cache',
  redis: { url: ENV.fetch('REDIS_URL'), driver: :hiredis }
}

require 'readthis'
cache = Readthis::Cache.new(
  expires_in: 2.weeks.to_i,
  redis: { url: ENV.fetch('REDIS_URL') }
)

REDIS_URL=redis://localhost:6379/2

Readthis::Cache.new(expires_in: 1.week)
Readthis::Cache.new(expires_in: 1.week.to_i)

```

```
```

