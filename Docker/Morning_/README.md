# Intro to Docker images
## Basic Docker commands

Listar imagenes en mi equipo
```bash
$ Docker images
```
Correr un contenedor
```bash
$ Docker run -it --name hola hello-world
```

Listar contenedores y su estado 
```bash
$ Docker ps -a
```
Eliminar un contenedor
```bash
$ Docker rm hola
```

## Docker hub
Docker Hub is a cloud-based registry service which allows you to link to code repositories, build your images and test them, stores manually pushed images, and links to Docker Cloud so you can deploy images to your hosts. It provides a centralized resource for container image discovery, distribution and change management, user and team collaboration, and workflow automation throughout the development pipeline.

Vamos a crear nuestra cuenta en el repositorio de imagenes publicas de Docker
Ir a: [Docker hub](https://hub.docker.com/)


```bash
$ Docker pull alpine 

$ Docker images

$ Docker rmi alpine
```

En la sesion de la tarde se creara una imagen en el equipo local y se sometera al repositorio publico.
