# Adminer Postgres Playground

This is a database dev environment using [docker](https://docs.docker.com/install/). I use it to make schemas, test SQL commands, and for development databases.

Pull up a local PostgresSQL 10 database using docker.

- `docker-compose up` to start postgres + adminer via Docker
- `docker-compose stop && docker-compose rm` to delete the containers

Access adminer at [http://localhost:5401/?pgsql=db&username=dev&db=DBplay](http://localhost:5401/?pgsql=db&username=dev&db=DBplay)

You might need to login with user `dev` and password `123`

## Init Script

On start up the init.sql script will be executed. Right now this creates an empty table called Sailors with three columns. To add multiple scripts that will run in alphabetical order add the following to the docker-compose.yml file under volumes:

`volumes:`
`	- ./v1_schema.sql:/docker-entrypoint-initdb.d/1-schema.sql`
`   - ./v2_schema.sql:/docker-entrypoint-initdb.d/2-schema.sql`