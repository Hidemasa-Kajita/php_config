# docker php environment

## environment
- infra
    - mysql80
    - php-fpm80
    - nginx
    - redis
- tool
    - redisinsight
        - redis client tool
    - schemaspay
        - DB schema
    - adminer
        - DB client tool
    - ※ minio
        - object storage

## how to use
- install [go-task](https://taskfile.dev/#/installation)
```
brew install go-task/tap/go-task
```

- execute command
```
# initialize environment
$ task build

# create container
$ task up
```

## access to browser
- your application
    - http://localhost:8000
- [redisinsight](https://redis.com/redis-enterprise/redis-insight/)
    - http://localhost:8001
- [schemaspay](https://github.com/schemaspy/schemaspy)
    - http://localhost:8002
- [adminer](https://www.adminer.org/)
    - http://localhost:8003
- [※ minio](https://min.io/)
    - http://localhost:8004

## task command
- task init
- task build
- task build:no-cache
- task up
- task up:d
- task stop
- task down
- task ps
