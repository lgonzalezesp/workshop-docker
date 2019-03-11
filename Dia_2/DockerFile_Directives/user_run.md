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
	
	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com

	USER user

	
**Parar el contenedor**

    docker stop <nombre de contenedor o id de la imagen>

**Agregar puerto de salida**

    docker run -d -p 80:80 nginx:latest

**Cambiar el puerto de salida**

    docker run -d -p 8080:80 nginx:latest

*Verificar la ejecución del nginx**

	elinks http://localhost



