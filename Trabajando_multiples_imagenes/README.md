# Workshop Docker 

## Trabajando con multiples imagenes

**Ejecutar un contenedor en modo interactivo**

    docker run -it ubuntu:xenial /bin/bash

**Ejecutar un contenedor en modo undergroud**

    docker run -itd ubuntu:xenial /bin/bash
    
**Información del contenedor**

    docker inspect <nombre del contenedor o ID>
    
**Obtener ip del contenedor**

	docker inspect <nombre del contenedor o ID> | grep IP
	
**Buscar imagen**

	docker search <nombre de la image / repositorio> ejemplo: docker search training/sinatra
	
