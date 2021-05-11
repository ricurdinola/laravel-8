# Docker: Web Stack
El proyecto tiene como objetivo instalar rápidamente un ambiente de desarrollo local para trabajar con [PHP](https://www.php.net/) y [MySQL](https://www.mysql.com/)
utilizando [Docker](https://www.docker.com). 

Stack Utilizado: Apache, MySQL, PHP, Composer y Node

## Requerimientos
* [Docker Desktop](https://www.docker.com/products/docker-desktop)

## Configurar el ambiente de desarrollo

A continuación, se explica brevemente la configuración a realizar en el archivo docker/.env dependiendo del proyecto:

* `COMPOSE_PROJECT_NAME`: El nombre al stack de contenedores que se generarán.

* `WEB_WERVER_NAME`: El nombre que le daremos al contenedor del servidor web

* `PHP_VERSION` versión de PHP ([Versiones disponibles de PHP](https://github.com/docker-library/docs/blob/master/php/README.md#supported-tags-and-respective-dockerfile-links)).

* `DB_SERVER_NAME`: El nombre que tendrá el contenedor del Mysql

* `MYSQL_DATABASE`: El Nombre de la Base de Datos a Crear.


Adicionalmente se pueden modificar otros parámetros, como ser:
* `PHP_PORT` puerto para servidor web.
* `MYSQL_VERSION` versión de MySQL([Versiones disponibles de MySQL](https://hub.docker.com/_/mysql)).
* `MYSQL_USER` nombre de usuario para conectarse a MySQL.
* `MYSQL_PASSWORD` clave de acceso para conectarse a MySQL.

## Estructura de Archivos

* `/docker/mysql` contiene el docker file de MySQL y la carpeta Data.
* `/docker/web-server` contiene el docker file de PHP.
* `/docker/web-server/config` contiene los directorios de configuración de apache y php. Estan los conf de apache y el .ini de php. Estos archivos se copian al contenedor al momento de generarlos. Si se modifican, será necesario regenerar los contenedores.
* `/www/` carpeta para los archivos Laravel del proyecto.

## Instalar el ambiente de desarrollo
Ingresar a la carpeta docker y ejecutar build.sh

