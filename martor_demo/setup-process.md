# Setup instructions

## First step

### Run start-server script

* Make it readable:
````
$ chmod 755 start-server.sh
````

* Make cache directory
```
$ mkdir -p .pip_cache
```

* Run docker
```
$ docker build -t django-markdown-editor .
```

### Run the docker container

```
$ docker run -it -p 8020:8020 \
     -e DJANGO_SUPERUSER_USERNAME=admin \
     -e DJANGO_SUPERUSER_PASSWORD=sekret1 \
     -e DJANGO_SUPERUSER_EMAIL=admin@example.com \
     django-markdown-editor
```

### Run the CI-CD

```
$ docker pull carke/django-markdown-editor
```
