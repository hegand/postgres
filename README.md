# Postgres docker image based on alpine

Minimal postgres image based on alpine linux and the official postgres image (init script).

## Usage:

### Quick start:

`docker run -d hegand/postgres:9.5`

### Add master password:

`docker run -d -e POSTGRES_PASSWORD=secretpass hegand/postgres:9.5`

### Attach a volume:

`docker run -d -e POSTGRES_PASSWORD=secretpass -v /local/dir:/var/lib/postgresql/data hegand/postgres:9.5`

## ENV VARIABLES:
### POSTGRES_PASSWORD
Set the postgres password. Recommended.

### POSTGRES_USER
Set the postgres user. Default: `postgres`.

### PGDATA
Set the pgdata directory. Default: `/var/lib/postgresql/data`.

### POSTGRES_DB
Set the default postgres db. If not set `POSTGRES_USER` will be used as a name.

### POSTGRES_INITDB_ARGS
Set inintdb arguments.

### POSTGRES_LISTEN_ADDRESSES
Set listen_addresses, default is `localhost`.

More info about the configs: [offical postgres image](https://hub.docker.com/_/postgres/)
