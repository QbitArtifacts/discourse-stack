# discourse-stack
Discourse installation for Docker Swarm based on bitnami images

## Configuration

```shell
cp .env .env.local  # create env file for stack
vi .env.local  # change ENV vars according to your needs
```

## Installation
Must have installed [docker](https://docs.docker.com/engine/install/) and
[docker-compose](https://docs.docker.com/compose/install/), and
[docker swarm](https://docs.docker.com/engine/swarm/swarm-tutorial/)
properly configured, for more info about swarm mode, there is a
[recommended reading](https://docs.docker.com/engine/swarm/key-concepts/).

Installation must be done from a manager node.
```shell
docker stack deploy -c <(docker-compose -f stack.yaml --env-file .env.local config) discourse
```