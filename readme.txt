Run the RedisMod container with:
docker run \
  -p 6379:6379 \
  -v `pwd`:/data \
  -v `pwd`/docker-redis.conf:/usr/local/etc/redis/redis.conf \
  --platform linux/amd64 \
  redislabs/redismod \
  /usr/local/etc/redis/redis.conf

The DB is persisted in the current working directory (with a default name)
The file docker-redis.conf is a custom config file. This is optional.


Run Redis Stack Server from binary with: 
redis-stack-server local-redis-stack.conf --dir "$(PWD)"

Uses the specified local-redis-stack.conf configuration file
Overrides the "dir" option to the working directory. If there is a dump.rdb in the local directory it will be picked up.