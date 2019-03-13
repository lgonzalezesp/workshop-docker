# Workshop Docker 

## Primeros Pasos

**Crear contenedor en modo interactivo**

    docker run -it ubuntu:xenial /bin/bash

**Crear archivo de ejemplo**

    cd /root
    echo "This is version 1 of our custom image " > test.txt
    apt-get update
    apt-get install telnet openssh-server
    adduser test
    which sshd
    which telnet
    cat /etc/group | grep test
    exit
    
**Ingresar de nuevo al contendor**

    docker ps -a 
    docker restart <nombre del contenedor o ID>
    docker attaach <nombre del contenedor o ID>
    
**Crear commit de los cambios**

	docker images
	docker commit -m "Already installed SSH and created test user" -a lgonzaleze <nombre de la imagen o ID>  lgonzaleze/ubusshd:v1
	
**Ingresar a Docker hub por CLI**

	docker login --username=yourhubusername --email=youremail@company.com
	
**Crar tag de la imagen**

	docker tag bb38976d03cf yourhubusername/verse_gapminder:firsttry
	
**Subir la imagen**

	docker push yourhubusername/verse_gapminder
	
