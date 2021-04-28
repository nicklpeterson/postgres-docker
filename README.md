# Adminer Postgres Playground

This is a database dev environment using [docker](https://docs.docker.com/install/). I use it to make schemas, test SQL commands, and for development databases.

Pull up a local PostgresSQL 10 database using docker.

- `docker-compose up` to start postgres + adminer via Docker
- `docker-compose stop && docker-compose rm` to delete the containers

Access adminer at [http://localhost:5401/?pgsql=db&username=dev&db=DBplay](http://localhost:5401/?pgsql=db&username=dev&db=DBplay)

You might need to login with user `dev` and password `123`