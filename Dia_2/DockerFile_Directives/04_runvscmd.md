# Workshop Docker 

## CMD VS RUN

**RUN**

Se ejecuta al momento de crear la imagen [build]

**CMD**

Se ejecuta al monendo de instanciar el contenedor [run]

**Crear carpeta y dockerfile**

	mkdir EchoServer
    vim Dockerfile

**Editar el archivo Dockerfile**

    #Dockerfile based on the latest CentOs 7 Image - non-privileged user entry
    FROM centos:latest
    MAINTAINER lgonzalez@altiuz.com

    RUN useradd -ms /bin/bash user
    CMD "echo" "This a custom container message for our LinuxAcademy Students"
    USER user
    
**Crear imagen**

    docker build -t="lgonzalez/ubuntuechoserver:v1" .

**Crear el contenedor**

    docker run lgonzalez/ubuntuechoserver:v1