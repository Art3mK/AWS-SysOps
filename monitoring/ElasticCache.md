# ElasticCache monitoring

- memcached
    * CPU > 90% -> add more nodes to cluster
- redis
    * not multi-threaded

- CPU
- Swap usage
    * no metric for redis, use **reserved-memory**
    * if > 50Mb - increase **memcached_connections_overhead** parameter
        * param defines memory to be reserved for memcached connections and other misc overhead
- Evictions
    * removes item from cache if space is needed
    * memcached
        * scale up
            * Scaling up however can NOT be done on the fly.
        * scale out
    * redis
        * scale out for clustered redis
        * scale up for single instances (without cluster mode enabled)
- Concurrent connections
    * set alarm

----
Links:
- https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/WhatIs.html
- https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/WhatIs.html