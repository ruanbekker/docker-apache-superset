# docker-apache-superset
Apache Superset on Docker

## Taskfile

Im using the [taskfile](https://taskfile.dev) build tool to simplify usage.

To install on a mac:

```
brew install go-task/tap/go-task
```

To install on linux: 

```
sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b /usr/local/bin
```

Then for help run:

```
task help
task: Available tasks for this project:
* backup: 	backup the project directory
* build: 	builds the containers specified in the docker-compose.yml
* default: 	runs by default and calls the help task
* deploy: 	deploys the containers from docker-compose.yml
* destroy: 	stops containers from docker-compose.yml
* help: 	prints out the help context
```

## Configuration

This should run as is, but configuration is specified in `docker-compose.yml` and environment variables defined in `docker/.env`.

For more information check out the main repo:
- https://github.com/apache/superset/tree/master/docker

## Usage

To build the containers:

```
task build
```

To deploy using docker-compose:

```
task deploy
```

Superset should be running on http://localhost:8088

## Resources

Official Superset Repo:
- https://github.com/apache/superset/tree/master/docker
