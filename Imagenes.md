# Servidor web
Arranca un contenedor que ejecute una instancia de la imagen php:7.4-apache, que se llame web y que sea accesible desde tu equipo en el puerto 8000.
![](Imagenes/imagen6.png)
Colocar en el directorio raíz del servicio web (/var/www/html) de dicho contenedor un fichero llamado index.html con el siguiente contenido:

## <h1>HOLA SOY XXXXXXXXXXXXXXX</h1>

Deberás sustituir XXXXXXXXXXX por tu nombre y tus apellidos.

![](Imagenes/imagen8.png)
Colocar en ese mismo directorio raíz un archivo llamado index.php con el siguiente contenido:
<?php echo phpinfo(); ?>

![](Imagenes/imagen9.png)

Para crear los ficheros tienes tres alternativas:
Ejecutando bash de forma interactiva en el contenedor y creando los ficheros.
Ejecutando un comando echo en el contenedor con docker exec.
Usando docker cp como hemos visto en el ejercicio 5.

## Servidor de base de datos
Arrancar un contenedor que se llame bbdd y que ejecute una instancia de la imagen mariadb para que sea accesible desde el puerto 3336.


Antes de arrancarlo visitar la página del contenedor en Docker Hub y establecer las variables de entorno necesarias para que:

La contraseña de root sea root.
Crear una base de datos automáticamente al arrancar que se llame prueba.
Crear el usuario invitado con las contraseña invitado.

![](Imagenes/imagen10.png)

Vemos los dos contenedores activos

![](Imagenes/imagen11.png)

Deberás entregar los siguientes pantallazos comprimidos en un zip o en un documento pdf:

Pantallazo que desde el navegador muestre el fichero index.html.

![](Imagenes/imagen12.png)

Pantallazo que desde el navegador muestre el fichero index.php.

![](Imagenes/imagen12.png)

Pantallazo donde se vea el tamaño del contenedor web después de crear los dos ficheros.

![](Imagenes/imagen13.png)

Pantallazo donde desde un cliente de base de datos (instalado en tu ordenador) se pueda observar que hemos podido conectarnos al servidor de base de datos con el usuario creado y que se ha creado la base de datos prueba (show databases). El acceso se debe realizar desde el ordenador que tenéis instalado docker, no hay que acceder desde dentro del contenedor, es decir, no usar docker exec.

![](Imagenes/imagen15.png)

Pantallazo donde se comprueba que no se puede borrar la imagen mariadb mientras el contenedor bbdd está creado.
