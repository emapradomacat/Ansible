# Aplicación "Reloj/Calendario" con Docker-Compose

Proyecto con despliegue Dockerizado que contiene una aplicación "Reloj/Calendario" desarrollada con Django (backend) y React.js (frontend). Muestra fecha y hora actual en un formato específico.


## Estructura 

proyecto/
- README.md
- docker-compose.yaml
- backend/
  - Dockerfile
  - Project/
    - views.py
    - setting.py
  - ...
- frontend/
  - Dockerfile
  - src/
    - App.js
    - App.css
  - ...


# ***Despliegue Local***
Sigue los pasos a continuación para compilar y desplegar la aplicación en tu entorno local.


## Requisitos Previos

Asegúrate de tener instalado lo siguiente antes de continuar:
- Python
- Docker
- Docker Compose


### 1. Clonar el repositorio
```
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

### 2. Desplegar con Docker-Compose

Ejecutar los siguientes comando desde el directorio raíz del proyecto. Esto creará y ejecutará los contenedores de Docker para el backend y el frontend de la aplicación.
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


# ***Despliegue en la Nube***
Sigue los pasos a continuación para compilar y desplegar la aplicación en la nube.


## Requisitos Previos

Asegúrate de tener en cuenta lo siguiente:
- Cuenta en el proveedor de servicios en la nube (por ejemplo, AWS, Google Cloud, Azure, etc.).
- Conocimiento básico sobre cómo trabajar con la plataforma en la nube seleccionada.


## Configuración del entorno en la nube

1. Crea una instancia de servidor virtual (VM) en la nube utilizando la plataforma elegida.
2. Configura las credenciales y permisos necesarios para acceder a los servicios de la nube (por 3.ejemplo, claves de API, roles de IAM, etc.).
3. Instala Docker y Docker Compose en la instancia de VM.
4. Clona el repositorio en la instancia de VM


## Configuración de variables de entorno
1. Configura las variables de entorno necesarias para el entorno de producción en la nube. Esto puede incluir configuraciones de bases de datos, claves de API, etc.
2. Asegúrate de proporcionar instrucciones claras sobre cómo establecer y gestionar las variables de entorno en la plataforma de la nube seleccionada.


## Despliegue de la aplicación
1. Navega hasta el directorio raíz del proyecto clonado en la instancia de VM.
2. Ejecuta el comando docker-compose up -d para iniciar los servicios de contenedores.
3. Verifica que los contenedores estén en funcionamiento correctamente ejecutando docker-compose ps.


## Escalado y administración
1. Proporciona instrucciones sobre cómo escalar la aplicación en la nube, en caso de que sea necesario.
2. Explica cómo monitorear y administrar los recursos en la nube, como el uso de registros de contenedores, supervisión de métricas, ajuste de escalado automático, etc.



## Autor

Este proyecto fue creado por Emanuel Prado Macat.
Cualquier consulta a emapradomacat@gmail.com -
