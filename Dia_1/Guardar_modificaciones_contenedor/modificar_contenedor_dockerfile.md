# Workshop Docker 

## Primeros Pasos

**Versión de Docker**

    docker version

**Información mas completa de docker**

    docker info
    
**Información de la capacidad actual**

    df -h
    
**Ir a la carpeta de Docker**

	cd /var/lib/docker/
	ll
	cd containers
	
**Mostrar contenedores en ejecución**

	docker ps
	
**Mostrar historial de ejecución de los contenedores**

	docker ps -a
	
**Descargar imagen de Ubuntu Xenial**

	docker pull ubuntu:xenial
	
**Crear contenedor Ubuntu Xenial y ejecutar /bin/bash**

	docker run -it ubuntu:xenial /bin/bash
	
**Ver programas en ejecución en Ubuntu**

	ps -aux
	
**Salir del contenedor y reiniciar el contenedor**

		exit
		docker restart <name container or Id>
		docker attach <name container or Id>

