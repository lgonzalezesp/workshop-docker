# Workshop Docker 

    

## Docker Hub
**Docker Hub** permite subir o utilizar imagenes oficiales de postgres, mysql .... y otros diferentes proyectos.
Visitar [hub.docker.com](https://hub.docker.com/) y crearse una cuenta en **Docker Hub**

## Instalar Docker sobre Centros OS 6 

Primero debemos crear el repositorio de Docker

    cd /etc/yum.repos.d/
    vim docker.repo
    
**docker.repo**

    [dockerrepo]
    name=DockerRepository
    baseurl=https://yum.dockerproject.org/repo/main/centos/$releasever/
    enabled=1
    gpgcheck=1
    gpgkey=https://yum.dockerproject.org/gpg

**Instalar Docker Engine**

    yum update
    sudo yum install docker-engine
    
**Iniciar Docker**

    sudo service docker start

**Parar Docker**

    sudo service docker stop
    
   **Agregar User al grupo de Docker**
	
	sudo usermod user -G docker

**Probar Docker**
	
	sudo usermod user -G docker
	reiniciar el equipo
**Probar Docker**

	docker run hello-world

    