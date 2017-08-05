# Docker Images

Primero vamos a crear una imagen apartir del Dockerfile

```bash
$ docker build -t dockerHubUser/pi .
```
Vamos a revisar que la imagen esta en nuestro inventario de imagenes

```bash
$ docker images
```
Corremos el contenedor a partir de la imagen que creamos
```bash
$ docker run --rm --name ejemploPi dockerHubUser/pi 100
```
## Docker hub

Vamos a cargar nuestra imagen al repositorio de Docker hub

```bash
$ docker push dockerHubUser/pi
```

Vamos a [DockerHub](https://hub.docker.com/) a revisar que nuestra imagen se encuentra ahora en un repositorio publico, y puedo descargarla desde cualquier equipo que cuente con Docker instalado.

## To go!

y que si no quiero subir mi imagen a un repositorio local, en lugar de eso quiero tener mi imagen de forma portable.

```bash
$ docker save --output="ejemplopi.tar" dockerHubUser/pi
$ ls -h
```

Para extraer en otro equipo
```bash
$ docker import ejemplopi.tar dockerHubUser/pi
```
Revisar que la imagen ha sido correctamente creada
```bash
$ docker images
```
