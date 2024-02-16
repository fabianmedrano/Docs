

# Docker Images

## Descarga de imagenes
  **Buscar en Docker Hub**
   - ver imagenes
   - ver versiones
   - ver banderas de configuración
 ```bash
     cd ~
     docker pull 
  ```
```bash
     cd ~
     docker pull name_image # descarga la ultima version de la imagen
  ```
```bash
     cd ~
     docker pull name_image:version # descarga la version de la imagen indicada
  ```
## Listado de imagenes

 ```bash
     cd ~
     docker images # muestra las imagenes que tenemos descargadas de docker
  ```

## Eliminar de imagenes
  **Buscar en Docker Hub**
   - ver imagenes
   - ver versiones
   - ver banderas de configuración
 ```bash
     cd ~
     docker image rm 
  ```
```bash
     cd ~
     docker image rm  name_image 
  ```
```bash
     cd ~
     docker image rm  name_image:version # elimina la version de la imagen indicada
  ```
----
----
----
----
----
----

# Docker Contenedores
## Descarga de imagenes
 importante revisar al banderas de configuracion particulares para cada contenedor en **docker hub**
 ```bash
     cd ~
     docker create 
  ```
```bash
     cd ~
     docker create --name nombre_con_el_que_vamos_a_nombrar_el_contenedor name_imagen # crear contenedor con nombre especifico
  ```
```bash
     cd ~
     docker create  -p27017:27017 --name nombre_contenedor name_imagen
# -p27017:27017 bandera para indicar los puertos,
#    el primero es para los puertos de la computadora fisica
#    el segundo son los puertos del contenerdor

## revisar cuales puertos se utilizan normalmente
  ```

## Listar contenerdores
 ```bash
     cd ~
     docker ps -a # mustra todos los contedores
  ```
## Iniciar contenerdor
 ```bash
     cd ~
     docker start 
  ```
 ```bash
     cd ~
     docker start id_contenedor
  ```
o
```bash
     cd ~
     docker start nombre_contenero
  ```
## Detener contenedor
 ```bash
     cd ~
     docker stop 
  ```
 ```bash
     cd ~
     docker stop id_contenedor
  ```
o
```bash
     cd ~
     docker start nombre_contenero
  ```
## Ver Logs contenedor
 ```bash
     cd ~
     docker logs --follow
  ```

 ```bash
     cd ~
     docker logs --follow name_contenedor
  ```
o
 ```bash
     cd ~
     docker logs --follow id_contenedor
  ```
----
----
----
----
----
----

# Docker Compose
La ventaja de usar Compose es que puedes definir la pila de tu aplicación en un archivo, mantenerlo en la raíz de tu repositorio de proyecto (ahora está bajo control de versiones) y permitir que otros contribuyan fácilmente a tu proyecto.

## Crear el archivo Compose**:
   - En el directorio de tu proyecto, crea un archivo llamado `docker-compose.yaml`.
   - Este archivo contendrá la definición de tus servicios (contenedores).

     ```yaml
     version: '3' # indica la versión de la sintaxis que se está utilizando 
     services:
       app:
         image: node:18-alpine #  Utiliza la imagen oficial de Node.js
         command: sh -c "yarn install && yarn run dev" # Ejecuta los comandos necesarios para iniciar tu aplicación
         ports:
           - 127.0.0.1:3000:3000 # Mapea el puerto 3000 del contenedor al puerto 3000 del host.
         working_dir: /app # Establece el directorio de trabajo dentro del contenedor.
         volumes: # Monta el directorio actual en el contenedor
           - ./:/app # .:/app: Esto significa que estás montando el directorio actual (donde se encuentra tu código fuente) en el contenedor en la ruta /app.
     # Cualquier cambio que realices en tu máquina local se reflejará automáticamente dentro del contenedor.
         environment: # Define las variables de entorno necesarias para tu aplicación.
           MYSQL_HOST: mysql
           MYSQL_USER: root
           MYSQL_PASSWORD: secret
           MYSQL_DB: todos
     ```

## Ejecutar la pila de la aplicación**:
   - Desde el directorio de tu proyecto, ejecuta:

     ```bash
     docker-compose up
     ```

   - Esto iniciará todos los servicios definidos en el archivo Compose.

## Verificar y detener la aplicación**:
   - Abre tu navegador y ve a `http://localhost:3000` para ver tu aplicación.
   - Cuando hayas terminado, ejecuta:

     ```bash
     docker-compose down
     ```

   - Esto detendrá y eliminará los contenedores.


----
----
----
----
----
----


**Docker Compose** para trabajar con **Laravel**, **MySQL**, **volúmenes** y **recarga en caliente (hot reload)**:

1. **Descargar Laravel y sus dependencias**:
   - Comencemos descargando la última versión de Laravel e instalando las dependencias necesarias para el proyecto, incluido **Composer**, el administrador de paquetes a nivel de aplicación para PHP. Utilizaremos Docker para evitar la instalación global de Composer.
   - Asegúrate de estar en tu directorio de inicio y clona la última versión de Laravel en un directorio llamado `laravel-app`:

     ```bash
     cd ~
     git clone ¹ laravel-app
     ```

   - Luego, entra al directorio `laravel-app`:

     ```bash
     cd ~/laravel-app
     ```

   - A continuación, utiliza la imagen de **Composer** de Docker para montar los directorios necesarios para tu proyecto Laravel y evitar la instalación global de Composer:

     ```bash
     docker run --rm -v $(pwd):/app composer install
     ```

   - El uso de las banderas `-v` y `--rm` con `docker run` crea un contenedor efímero que se montará en tu directorio actual antes de ser eliminado. Esto copiará el contenido de tu directorio `~/laravel-app` al contenedor y también asegurará que la carpeta `vendor` que Composer crea dentro del contenedor se copie a tu directorio actual.
   - Como último paso, establece los permisos en el directorio del proyecto para que pertenezca a tu usuario no root:

     ```bash
     sudo chown -R $USER:$USER ~/laravel-app
     ```

   - Esto será importante cuando escribas el **Dockerfile** para la imagen de tu aplicación en el **Paso 4**, ya que te permitirá trabajar con el código de tu aplicación y ejecutar procesos en tu contenedor como un usuario no root.

2. **Crear un archivo docker-compose.yaml**:
   - Ahora vamos a definir toda la configuración de la pila (Laravel, Nginx, MySQL) en un archivo `docker-compose.yaml`.
   - Aquí tienes un ejemplo básico de un archivo Compose para Laravel, MySQL y volúmenes con recarga en caliente:

 
```yaml
    version: '3' # indica la versión de la sintaxis que se está utilizando 
    services:
      # Servicio web para Laravel y Nginx
      web:
        build: .
        ports:
          - "80:80"  # Mapea el puerto 80 del host al puerto 80 del contenedor
        volumes:
          - ./laravel-app:/var/www/html  # Monta el directorio local en el contenedor
        environment:
          - APP_ENV=local  # Configura el entorno de la aplicación como local
          - APP_DEBUG=true  # Habilita el modo de depuración
      # Servicio de base de datos MySQL
      db:
        image: mysql:5.7
        environment:
          MYSQL_ROOT_PASSWORD: secret  # Contraseña de root para MySQL
          MYSQL_DATABASE: laravel  # Nombre de la base de datos
          MYSQL_USER: laravel  # Usuario de la base de datos
          MYSQL_PASSWORD: laravel  # Contraseña del usuario
        volumes:
          - db-data:/var/lib/mysql  # Monta un volumen para almacenar los datos de la base de datos
    volumes:
      db-data:  # Define el volumen llamado "db-data"
```

----
----
----
----
----
----

¡Buena pregunta! En **Docker Compose**, puedes organizar tus servicios de diferentes maneras. Aquí tienes algunas opciones:

1. **Definir todos los servicios en un solo archivo**:
   - Puedes listar todos tus servicios directamente en el archivo `docker-compose.yaml`.
   - Esto es simple y funciona bien para proyectos pequeños o medianos.
   - Sin embargo, si tienes muchos servicios, el archivo puede volverse largo y difícil de mantener.

2. **Dividir tus servicios en varios archivos**:
   - Puedes crear múltiples archivos de Compose y luego combinarlos según tus necesidades.
   - Por ejemplo, puedes tener un archivo base con servicios comunes y luego archivos adicionales para entornos específicos o servicios únicos.
   - Aquí tienes un ejemplo:

     ```yaml
     # docker-compose.yaml (archivo base)
     version: '3'
     services:
       common-service:
         image: myapp:latest
         # Configuración común aquí

     # docker-compose.dev.yaml (archivo específico para desarrollo)
     version: '3'
     services:
       dev-service:
         extends:
           file: docker-compose.yaml
           service: common-service
         # Configuración adicional para desarrollo

     # docker-compose.prod.yaml (archivo específico para producción)
     version: '3'
     services:
       prod-service:
         extends:
           file: docker-compose.yaml
           service: common-service
         # Configuración adicional para producción
     ```

   - Luego, puedes ejecutar Compose con:

     ```bash
     docker-compose -f docker-compose.yaml -f docker-compose.dev.yaml up
     ```

     o

     ```bash
     docker-compose -f docker-compose.yaml -f docker-compose.prod.yaml up
     ```

3. **Herencia de servicios**:
   - Puedes usar la palabra clave `extends` para heredar servicios de otro archivo.
   - Por ejemplo:

     ```yaml
     # docker-compose.yaml
     version: '3'
     services:
       service-one:
         image: myapp:latest

     # docker-compose.prod.yaml
     version: '3'
     services:
       service-two:
         extends:
           file: docker-compose.yaml
           service: service-one
         environment:
           BACKEND: some_other_value
     ```

   - Aquí, `service-two` hereda de `service-one` y agrega configuración adicional.

