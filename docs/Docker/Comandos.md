---
layout: default
title: Comandos
nav_order: 1
has_children: false
parent: Docker
---

# Comandos

## Imagenes
```bash
# Listar imagenes
$ docker images

# Construir imagen
$ docker build -t [image-name]:[image-tag] -f [new-dockerfile-name] [location]

# Eliminar imagen
$ docker rmi <image-id>

# Eliminar todas las imagenes
$ docker rmi -f $(docker images ps -aq)
```

## Contenedores
```bash
# Listar contenedores en ejecucion
$ docker ps

# Listar contenedores recientes
$ docker ps -a

# Crear contenedor
$ docker run -d [image-name]:[image-tag]
$ docker run -d --name [container-name] -p [port-machine]:[port-container] [image-name]:[image-tag]
$ docker run -d --name [container-name] -p [port-machine]:[port-container] -e "[variable-environment-name]=[variable-environment-value]" [image-name]:[image-tag]
$ docker run -d --name [container-name] -p [port-machine]:[port-container] -v  [folder-volume-machine]:[folder-volume-container] [image-name]:[image-tag]
$ docker run -d --network [network-name] --name [container-name] -p [port-machine]:[port-container] -v  [folder-volume-machine]:[folder-volume-container] [image-name]:[image-tag]

# Renombrar contenedor
$ docker rename [filename-old] [filename-new]

# Parar contenedor
$ docker stop [container-id]

# Iniciar Contenedor
$ docker start [container-id]

# Reiniciar Contenedor
$ docker restart [container-id]

# Borrar todos los contenedores
$ docker rm -fv $(docker ps -aq)

# Eliminar contenedor
$ docker rm -f [container-id]

# Acceder dentro de un contenedor
$ docker exec -ti [container-id] bash

# Pausa un contenedor en ejecución, "congelándolo" en su lugar
$ docker pause [container-id]
$ docker unpause [container-id]
```

## Volumenes
```bash
# Crear volumen
$ docker volume create [volume-name]

# Listar volúmenes
$ docker volume ls
```

## Redes
```bash
# Inspeccionar Network
$ docker inspect network [network-name]

# Crear una red
$ docker network create [network-name]

# Listar Networks
$ docker network ls

# Agregar contenedores
$ docker run -d --name [network-name] [container-name]

# Conectar contenedor existente a una red distinta
$ docker network connect [network-to-connect] [container-name-to-connect]

# Desconectar red
$ docker network disconnect [network-name]

# Eliminar red
$ docker network rm [network-name]
```
