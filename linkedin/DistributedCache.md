Design and implement a cache which has a capacity. Dump the lowest ranked element if the cache is full.
然后就是追问怎么设计distributed cache system。

LRU: doublelinklist + unordered_map

Distributed Cache
The cache is sharded across all machines in the cache cluster - More complex, although it is likely the best option. We could use hashing to determine which machine could have the cached results of a query using machine = hash(query). We'll likely want to use consistent hashing.
