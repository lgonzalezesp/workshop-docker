# Workshop Docker 

## Expose

**EXPOSE**

Permite exponer un puerto de nuestro contenedor
**Crear carpeta y dockerfile**
	mkdir ApacheInstallation
    cd ApacheInstallation
    vim Dockerfile

**Editar el archivo Dockerfile**

    #Dockerfile based on the latest CentOs 7 Image - non-privileged user entry
    FROM centos:latest
    MAINTAINER lgonzalez@altiuz.com
    RUN yum  update -y
    RUN yum install -y httpd net-tools

    RUN echo "this is a custom index file build during the image creation" > /var/www/html/index.html
    EXPOSE 80
    ENTRYPOINT apachectl "-DFOREGROUND"
    
**Crear imagen**
    docker build -t lgonzalez/centosapache:v1 .

**Crear el contenedor**

    docker run --name apacheweb1 -p 8080:80 lgonzalez/centosapache:v1

    docker run --name apacheweb1 -P lgonzalez/centosapache:v1