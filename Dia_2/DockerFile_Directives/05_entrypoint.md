# Workshop Docker 

## ENTRYPOINT

**ENTRYPOINT**

Se ejecuta al momento de crear la imagen pero no permite su modificación , se utiliza especialmente para como un ejecutable

**Crear carpeta y dockerfile**

	mkdir EntryServer
    vim Dockerfile

**Editar el archivo Dockerfile**

    #Dockerfile based on the latest CentOs 7 Image - non-privileged user entry
    FROM centos:latest
    MAINTAINER lgonzalez@altiuz.com

    RUN useradd -ms /bin/bash user
    ENTRYPOINT echo "This a custom container message for our LinuxAcademy Students"
    USER user
    
**Crear imagen**
    docker build -t="lgonzalez/ubuntuentryserver:v1" .

**Crear el contenedor**

    docker run lgonzalez/ubuntuentryserver:v1