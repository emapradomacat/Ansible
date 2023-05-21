# Aplicación "Reloj/Calendario" con Docker-Compose

Proyecto con despliegue Dockerizado que contiene una aplicación "Reloj/Calendario" desarrollada con Django (backend) y React.js (frontend). Permite mostrar la fecha y hora actual en un formato específico.

## Requisitos Previos

Asegúrate de tener instalado lo siguiente antes de continuar:

- Docker
- Docker Compose

## Instrucciones de compilación y despliegue local

Sigue los pasos a continuación para compilar y desplegar la aplicación en tu entorno local.


### 1. Clonar el repositorio
```
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

### 2. Desplegar con Docker-Compose

Esto creará y ejecutará los contenedores de Docker para el backend y el frontend de la aplicación.
```
docker-compose build
docker-compose up
```

### 3. Acceder a la aplicación

Una vez que los contenedores estén en ejecución, podrás acceder a la aplicación en tu navegador web en la siguiente dirección:

http://localhost:3000

¡Y eso es todo! Ahora deberías ver la aplicación de Reloj/Calendario funcionando en tu entorno local.


### 4. Resultado Esperado

La lista de contenedores debe mostrar dos contenedores en ejecución y el mapeo de puertos de la siguiente manera:

```
$docker ps
```
```
CONTAINER ID   IMAGE              COMMAND                  CREATED         STATUS         PORTS                                       NAMES
53c15d00c4b0   django-react-api   "bash -c 'python man…"   2 minutes ago   Up 2 minutes   0.0.0.0:8000->8000/tcp, :::8000->8000/tcp   django-react-api-1
c493f03a70f9   django-react-web   "docker-entrypoint.s…"   2 minutes ago   Up 2 minutes   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   django-react-web-1
```


### 5. Detener y eliminar contenedores

```
docker-compose down
```


## Instrucciones de compilación y despliegue en la Nube

Si deseas desplegar la aplicación en la nube, puedes seguir los siguientes pasos:

1. Configura una cuenta en el proveedor de nube de tu elección (por ejemplo, AWS, GCP, Azure).
2. Crea una instancia o máquina virtual en la nube.
3. Instala Docker y Docker Compose en la instancia o máquina virtual.
4. Clona el repositorio en la instancia o máquina virtual.
5. Compila y ejecuta los contenedores Docker utilizando el comando docker-compose up.
6. Configura las reglas de firewall y la configuración de red necesarias para permitir el acceso a  a aplicación desde Internet.
7. Obtén la dirección IP o el nombre de dominio público de la instancia o máquina virtual.
8. Accede a la aplicación utilizando la dirección IP o el nombre de dominio público seguido del puerto 3000 en tu navegador web.
9. Recuerda consultar la documentación y las guías de tu proveedor de nube específico para obtener instrucciones detalladas sobre cómo desplegar aplicaciones en la nube.



## Autor

Este proyecto fue creado por Emanuel Prado Macat.
