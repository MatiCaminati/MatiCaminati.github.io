# Dockers

Docker se encarga de  crear contenedores ligeros y portables para las aplicaciones software que puedan ejecutarse en cualquier máquina con Docker instalado, independientemente del sistema operativo que la máquina tenga por debajo, facilitando de este modo los despliegues.

Docker, permite meter en un contenedor todas aquellas cosas que una aplicación necesita para ser ejecutada y la propia aplicación. Así se puede llevar ese contenedor a cualquier máquina que tenga instalado Docker y ejecutar la aplicación sin tener que hacer nada más, ni preocuparse de qué versiones de software tiene instalada esa máquina, de si tiene los elementos necesarios para que funcione la aplicación , de si son compatibles,etc.

#### Instalación:

1. Eliminar versiones ya instaladas:

        sudo apt-get remove docker docker-engine docker.io containerd runc
2. Actualice el apt índice de paquetes e instale paquetes para permitir el apt uso de un repositorio sobre HTTPS:

        sudo apt-get update

        sudo apt-get install \
	    apt-transport-https \
	    ca-certificates \
	    curl \
	    gnupg \
	    lsb-release

3. Agregue la clave GPG oficial de Docker:

        curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

4. Actualizar el apt índices nuevamente:

        sudo apt-get update

5. Actualice el apt índice del paquete e instale la última versión de Docker Engine y containerd:

        sudo apt-get update

        sudo apt-get install docker-ce docker-ce-cli containerd.io


#### Manejo básico de contenedores:

##### Imagen

La imagen es la configuración necesaria con la cual se puede construir un contenedor.

Para descargar una imagen, en este caso la versión más reciente de ubuntu:

    docker pull ubuntu:latest

Ver imágenes disponibles:

    docker images

Borrar imagne:

    docker rmi 'IMAGE_ID' 

Crear una imagen a partir de un contenedor:

    docker commit 'CONTAINER_ID' image_name:tag

##### Contenedores

- Crear un contenedor, en este caso con la imagen de ubuntu:

        docker run -it ubuntu

- Salir del contenedor:

        contenedor:/# exit

- Levantar un contenedor:

        docker start 'CONTAINER_ID'

- Entrar a un contenedor que esté corriendo:

    opción 1:

        docker exec -ti 'ID del contenedor' /bin/bash

    opción 2:

        docker attach 'ID del contenedor'

- Ver contenedores:

        docker ps -a

- Borrar contenedor:

        docker container rm 'ID del contenedor'