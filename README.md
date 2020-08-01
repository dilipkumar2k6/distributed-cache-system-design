# Functional requirement
- Cache is high speed data storage system
- It saves the transient data
- On further request, it will not hit the main memory or not compute the actual computation
- All the data will be served from the cache system
- Data in cache system stored in RAM
# Caching best practices
- Validity
- High hit rate
- Cache miss
- TTL
# Design constraints
- Tera bytes of data
- 50K to 1 million QPS
- 1ms latency
- LRU (eviction)
- 100% availability 
- Scalable
# Cache access pattern
## Write through 
On write:
- Write into cache
- Write into DB as well
- After that response will be return
On read:
- Read from cache
## Write around
On write:
- Write will go to DB first
- It will not be written into cache
On read: 
- Cache will get the data from DB
- Write into cache
- return response
## Write back
On write:
- Data will be written in cache 
- Response will be return
- There is async process which will take data from cache and write into DB
# HashTable
# Cache eviction
- 