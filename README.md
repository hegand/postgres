# Postgres docker image based on alpine

Minimal postgres image based on alpine linux and the official postgres image (init script).

## Usage:

### Quick start:

`docker run -d hegand/postgres:9.5`

### Add master password:

`docker run -d -e POSTGRES_PASSWORD=secretpass hegand/postgres:9.5`

### Attach a volume:

`docker run -d -e POSTGRES_PASSWORD=secretpass -v /local/dir:/var/lib/postgresql/data hegand/postgres:9.5`

More info about the configs: [offical postgres image](https://hub.docker.com/_/postgres/)
