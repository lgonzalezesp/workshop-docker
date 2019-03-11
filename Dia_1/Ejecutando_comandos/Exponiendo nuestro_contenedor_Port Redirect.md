# Workshop Docker 

## Exponiendo nuestro contenedor con Port Redirect

**Visitar la página de nginx en docker hub**

    https://hub.docker.com/_/nginx

**Correr el contenedor de nginx en mode demonio**

    docker run -d nginx:latest
    
**Obtener la ip del contenedor de nginx**

    docker inspect <nombre de contenedor o id de la imagen> | grep IPAddress

**Verificar la ejecución del nginx**
	elinks http://172.17.0.1

**Parar el contenedor**

    docker stop <nombre de contenedor o id de la imagen>

**Agregar puerto de salida**

    docker run -d -p 80:80 nginx:latest

**Cambiar el puerto de salida**

    docker run -d -p 8080:80 nginx:latest

*Verificar la ejecución del nginx**

	elinks http://localhost



