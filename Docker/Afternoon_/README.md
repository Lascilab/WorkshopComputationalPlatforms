# Docker Images
Primero vamos a configurar el pc actual con nuestro usuario de Docker Hub

```bash
$ export DOCKER_ID_USER="username"
```
Login 
```bash
$ docker login
```

Primero vamos a crear una imagen apartir del Dockerfile

```bash
$ docker build -t $DOCKER_ID_USER/pi_image .
```
Vamos a revisar que la imagen esta en nuestro inventario de imagenes

```bash
$ docker images
```
Corremos el contenedor a partir de la imagen que creamos
```bash
$ docker run --rm --name ejemploPi $DOCKER_ID_USER/pi_image 100
```
## Docker hub

Vamos a cargar nuestra imagen al repositorio de Docker hub

```bash
$ docker push $DOCKER_ID_USER/pi_image
```

Vamos a [DockerHub](https://hub.docker.com/) a revisar que nuestra imagen se encuentra ahora en un repositorio publico, y puedo descargarla desde cualquier equipo que cuente con Docker instalado.

## To go!

y que si no quiero subir mi imagen a un repositorio local, en lugar de eso quiero tener mi imagen de forma portable.

```bash
$ docker save --output="ejemplopi.tar" $DOCKER_ID_USER/pi_image
$ ls -h
```

Para extraer en otro equipo
```bash
$ docker import ejemplopi.tar $DOCKER_ID_USER/pi_image
```
Revisar que la imagen ha sido correctamente creada
```bash
$ docker images
```
