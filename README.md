django-redis-sessions
=======================
Redis database backend for your sessions (with plain json session storage)


Installation
============

* Run `pip install django-redis-sessions` or alternatively  download the tarball and run `python setup.py install`,

* Set `redis_sessions.session` as your session engine, like so:


```
SESSION_ENGINE = 'redis_sessions.session'
```

* Optional settings:

```
SESSION_REDIS_HOST = 'localhost'
SESSION_REDIS_PORT = 6379
SESSION_REDIS_DB = 0
SESSION_REDIS_PASSWORD = 'password'
SESSION_REDIS_PREFIX = 'session'
SESSION_REDIS_SOCKET_TIMEOUT=1

# If you prefer domain socket connection, 
# you can just add this line instead of SESSION_REDIS_HOST and SESSION_REDIS_PORT.

SESSION_REDIS_UNIX_DOMAIN_SOCKET_PATH = '/var/run/redis/redis.sock'

# Redis Sentinel 
SESSION_REDIS_SENTINEL_LIST = [(host, port), (host, port), (host, port)]
SESSION_REDIS_SENTINEL_MASTER_ALIAS = 'sentinel-master'

```
