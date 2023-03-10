# DJANGO


## Dependencies

* [Python](https://www.python.org/) 3.7
* [Django](https://www.djangoproject.com/) 2.1

## Get Started

```
$ docker-compose up --build
```

### Development

- Main site
    - http://localhost:8000

- Admin page
    - http://localhost:8000/admin

### Commands

run migrations: 
```
$ docker exec python ./manage.py migrate
```

#### General
create a django app
```
$ docker exec python ./manage.py startapp {app_label}
```

create models from existing database
```
$ docker exec python ./manage.py inspectdb > {path/to/models.py}
```

execute migration
```
$ docker exec python ./manage.py migrate
```

create a migration file
```
$ docker exec python ./manage.py makemigrations
```

create dump fixture files
```
$ docker exec python ./manage.py dumpdata {app_label.model} --indent 2 > {path/to/fuxture.json}
```

load data from fixture files
```
$ docker exec python ./manage.py loaddata --verbosity 2 > {path/to/fuxture.json}
```

create an admin account
```
$ docker exec -it python ./manage.py createsuperuser
```