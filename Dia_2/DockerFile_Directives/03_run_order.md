# Workshop Docker 

## Orden de ejecución

**Crear Carpeta Build / RunAsUser**

    mkdir builds
    cd builds
    mkdir CustomMessage

**Crear archivo Dockerfile**

    vim Dockerfile

**Dockerfile con usuario user**
	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com

	RUN useradd -ms /bin/bash user
	USER user

	RUN echo "export 192.168.0.0/24" >> /etc/export.list

**Cambiar el orden de ejecución para que se ejecute como root**

	FROM centos:latest
	MAINTAINER lgonzalez@altiuz.com

	RUN useradd -ms /bin/bash user
	RUN echo "export 192.168.0.0/24" >> /etc/export.list
	USER user


