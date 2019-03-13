# Workshop Docker 

## Docker Directives USER and RUN

**Crear Carpeta Build / RunAsUser**

    mkdir builds
    cd builds
    mkdir RunAsUser

**Eliminar un contenedor**

    docker rmi <nombre del contenedor o Id>
    
**Crear archivo Dockerfile**

    vim Dockerfile

**Dockerfile con usuario user**
	# Dockerfile RunAsUser
	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com

	USER user

	
**Crear la imagen**

    docker build -t centos7/nonroot:v1 .

**Crear contenedor**

    docker run -it centos7/nonroot:v1 /bin/bash

    docker: Error response from daemon: linux spec user: unable to find user user: no matching entries in pas

**Modifiquemos el dockerfie para que permite ejecutar el bin/bash**

    FROM centos:latest
    MAINTAINER lgonzalez@altiuz.com

    RUN useradd -ms /bin/bash user
    USER user

**Parar ingresar al contenedor como usuario root**

    docker exec -u 0 -it <nombre del contenedor o ID> /bin/bash


