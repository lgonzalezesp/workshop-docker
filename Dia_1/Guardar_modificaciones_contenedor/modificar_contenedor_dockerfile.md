# Workshop Docker 

## Crear imagen por medio de un Dockerfile

**Crear Carpeta build**

    mkdir build
    cd build

**Crear archivo Dockerfile**

    vim Dockerfile
    
**Editar el contenido del dockerfile**

    #this is a custom ubuntu image with ssh already installed
    FROM ubuntu:xenial
	MAINTAINER lgonzalez <lgonzalez@altiuz.com>
	RUN apt-get update
	RUN apt-get install telnet openssh-server

    
**Contruir la imagen**

	docker build -t="lgonzalez/ubuntusshonly:v2" .
	
**Agregar -y para forzar la respuesta (yes)**

	#this is a custom ubuntu image with ssh already installed
    FROM ubuntu:xenial
	MAINTAINER lgonzalez <lgonzalez@altiuz.com>
	RUN apt-get update
	RUN apt-get install -y telnet openssh-server
	
**Contruir la imagen**

	docker build -t="lgonzalez/ubuntusshonly:v2" .

**Verificar la instalación de ssh**

	which sshd