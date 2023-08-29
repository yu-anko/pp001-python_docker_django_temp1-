# how to use django on docker

## create project

```bash
docker-compose run web django-admin startproject myproject .
```


## create docker image
    
```bash
docker-compose build
```

## create docker container

```bash
docker-compose up -d
```

以下にアクセス
http://127.0.0.1:8000/