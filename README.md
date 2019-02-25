# DPiHole

DPiHole is a project that allows to deploy a PiHole in a distributted environment like Docker Swarm

## Requirements
- Docker

## Usage

### Docker Swarm
Docker Swarm rocks!! Could be easier?
```
docker stack deploy -c docker-compose.yml dpihole
```

### Docker-Compose
Docker-compose doesn't support deploy params. If you launch it outside a Docker Swarm, probably this params would be ignored.
Starting up a container with DPiHole service (probably without deploy params)
```
docker-compose up
```
### Customize running
Environment file was added to provide a separate path for common configurations in a DPiHole deployment.
All variables must been provided.