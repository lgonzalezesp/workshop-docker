# Workshop Docker 

## Variables de entorno

**Crear Carpeta Build / RunAsUser**

    mkdir builds
    cd builds
    mkdir JavaInstall

**Crear archivo Dockerfile**

    vim Dockerfile

**Dockerfile con Java 8**
	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com
	RUN useradd -ms /bin/bash user
	RUN echo "export 192.168.0.0/24" >> /etc/export.list
	RUN yum install -y java-1.8.0-openjdk
	USER user

	RUN cd ~ && echo "export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.201.b09-2.el7_6.x86_64" >> /home/user/.bashrc

**Construir imagen del dockerfile**

	docker build -t centos7/java8:v1 .

**Creamos un contenedor en base la imagen**
	
	docker run -it centos7/java8:v1 /bin/bash

**Verificamos que este creada la variable de ambiente**

	> env

**Creamos una variable de entorno con ENV**
	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com
	RUN useradd -ms /bin/bash user
	RUN echo "export 192.168.0.0/24" >> /etc/export.list
	RUN yum install -y java-1.8.0-openjdk
	USER user

	RUN cd ~ && echo "export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.201.b09-2.el7_6.x86_64" >> /home/user/.bashrc

	ENV JAVA_BIN /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.201.b09-2.el7_6.x86_64/jre/bin
