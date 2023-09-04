# how to use django on docker

## create project

```bash
docker-compose run web django-admin startproject myproject .
```

## DBを以下の様に変更
myproject/settings.py
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'mydatabase',
        'USER': 'myuser',
        'PASSWORD': 'mypassword',
        'HOST': 'db',
        'PORT': 5432,
    }
}

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