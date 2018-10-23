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

Readthis::Cache.new(refresh: true)

config.cache_store = :readthis_store, {
  compress: true,
  compression_threshold: 2.kilobytes
}

Readthis::Cache.new(marchal: Readthis::Passthrough)

Readthis.serializers << obj

Readthis.serializers.freeze!
Readthis::Cache.new(marshal: Oj)

Readthis.fault_tolerant = true

Rails.cache.pool.with { |client| client.expire('foo-key', 60) }
```

```
```

