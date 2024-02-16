
# Docker Images
## Listado de imagenes

 ```bash
     cd ~
     docker images # muestra las imagenes que tenemos descargadas de docker
  ```

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
    version: '3'
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
