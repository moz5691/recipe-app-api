# recipe-app-api
Django application 

```shell
docker-compose run app sh -c "django-admin.py startproject app ." 
```

```shell
 docker-compose run app sh -c "python manage.py startapp core"
```

In every time changing the model, rerun the following makemigrations again.
```shell
docker-compose run app sh -c "python manage.py makemigrations core"
```


There are two different ways.

```shell
docker-compose build up -d 
docker-compose exec app python manage.py test
```
Note that ```docker-compose exec``` is meant to interact with containter that is already running.
It is best to use ```docker-compose up``` to run the service or services as they would normally execute.

or
```shell
docker-compose run app sh - c "python manage.py test"
```
It is best to use ```docker-compose run``` to run one-off processes/tasks that support the services.

