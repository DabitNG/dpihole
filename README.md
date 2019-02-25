# DPiHole

DPiHole is a project that allows to deploy a PiHole in a distributted environment like Docker Swarm

## Requirements
- Docker

## Usage

### Docker Swarm
Docker Swarm rocks!! Could be easier?
```
./start.sh
```

If you want to customize any param like your stack name, use the following command:
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
All variables must been provided. This is a preview of default configuration
```
PIHOLE_HOSTNAME=dpihole
PIHOLE_PORT=80
PIHOLE_IP=192.168.1.150
PIHOLE_DNS1=127.0.0.1
PIHOLE_DNS2=1.1.1.1
PIHOLE_PASS=myadminpassword
```
## Test

This environment was tested in the following environments:
- RPi with Hypriot (I&O Docker Swarm)
- Boot2Docker with VirtualBox over Windows 10 Home
- Docker version 18.03.0-ce, build 0520e24302
- Docker version 18.04.0-ce, build 3d479c0
- docker-compose version 1.20.1, build 5d8c71b2
- docker-compose version 1.21.1, build 5a3f1a3
