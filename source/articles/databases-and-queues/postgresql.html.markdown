---
title: PostgreSQL
tags: database
category: Databases and Queues
---

# PostgreSQL

+ [Create Databases and run psql commands](#create-db)
+ [Enable Extensions](#extensions)
+ [PostGIS](#postgis)
+ [Ruby on Rails](#ruby-on-rails)
+ [Django](#django)


The default databases created for you are **development** and **test**.

PostgreSQL ```9.2.4``` runs on the default port and the credentials are stored in the ```PG_USER``` and ```PG_PASSWORD``` environment variables.

We install the Ubuntu postgresql-contrib package. It includes the extension modules listed in the [PostgreSQL Documentation](http://www.postgresql.org/docs/9.2/static/contrib.html).

You need to activate them with ```CREATE EXTENSION``` as explained in the [Extension Guide](http://www.postgresql.org/docs/9.1/static/sql-createextension.html).

## [Create Databases and run psql commands](#create-db){:name="create-db"}
You can run any SQL query against the PostgreSQL database. For example to create a new database:

~~~shell
psql -c 'create database new_db;'
~~~

## [Enable Extensions](#extensions){:name="extensions"}
You can enable extensions either in your database migrations or by running the commands against the database. For example, to enable hstore for the test database:

~~~shell
psql -c 'create extension hstore;' -d test
~~~

in your setup commands.

## [PostGIS](#postgis){:name="postgis"}
PostGIS 2.0.x is installed on the virtual machine.

## [Ruby on Rails](#ruby-on-rails){:name="ruby-on-rails"}

We replace the values in your `database.yml` automatically.

## [Django](#django){:name="django"}

~~~python
DATABASES = {
  'default': {
    'ENGINE': 'django.db.backends.postgresql_psycopg2',
    'NAME': 'test',
    'USER': os.environ.get('PG_USER'),
    'PASSWORD': os.environ.get('PG_PASSWORD'),
    'HOST': '127.0.0.1',
  }
}
~~~

