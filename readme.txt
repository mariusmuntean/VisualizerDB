Run the Redis Stack container with:
docker run -p 6379:6379 -p 8001:8001 -v "$(pwd)":/data -v "$(pwd)"/local-redis-stack.conf:/redis-stack.conf redis/redis-stack:latest

Port 6379 is the default Redis server port
Port 8001 is the default Redis Insight port
The DB is persisted in the current working directory (with a default name)
The file local-redis-stack.conf is a custom config file. This is optional.
