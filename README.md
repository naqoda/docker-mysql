# Supported tags and respective `Dockerfile` links

-	[`latest`]

# Info
Based on [mysql:latest] (https://hub.docker.com/_/mysql/) image with addition of:

```console
[mysqld]
sql_mode=NO_ENGINE_SUBSTITUTION
default-storage-engine = innodb
```

And UTF-8 configuration:

```console
[mysqld]
character-set-server = utf8'
collation-server = utf8_unicode_ci
[client]
default-character-set=utf8
```

# Run
Run this image:

```console
$ docker run --name mysql \
	-e MYSQL_ROOT_PASSWORD=root \
	-d naqoda/mysql:latest
```