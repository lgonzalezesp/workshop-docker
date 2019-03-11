# Workshop Docker 

## Ejecutando comandos con Docker

**Ver el log de un contenedor**

    docker logs <nombre del contenedor>

**Ejecutar un comando dentro de un contendor**

    docker exec <nombre del contenedor> /bin/cat /etc/profile
    
**Ejecutar un contenedor como demonio**

    docker run -d ubuntu:xenial /bin/bash -c "while true;do echo HELLO;sleep 1;done"

**Contar las lienas del log**

    docker logs <nombre del contenedor> | wv -l
