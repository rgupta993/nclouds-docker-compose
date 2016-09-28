# Nclouds Docker compose

This repo contains two docker compose apps:

1. One docker compose app is contained in directory `docker-compose-app`. This composition uses links to link redis container with node app.

2. Second docker compose app is contained in directory `docker-compose-consul-app`. This composition uses `consul` for service discovery. This app deploys two node app containers, one redis container, one consul server container and one registrator.

### Prerequisites

* docker
* docker-compose

### Usage

1. Clone the repo

For deploying:

1st app:

```
$ cd docker-compose-app
$ docker-compose up -d
```

2nd app:

```
$ cd docker-compose-consul-app
$ source generate-docker-compose.sh; rm -rf docker-compose.yml; envsubst < "docker-compose-template.yml" > "docker-compose.yml";
$ docker-compose up -d
```

After the deployment, api's can be accessed. More info about the same can be found [here](https://github.com/rgupta993/nclouds-app#apis).
