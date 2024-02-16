## Servidor FTP
_"Los servidores de FTP son aplicaciones de software que posibilitan la transferencia de archivos de un dispositivo (es decir, una computadora con Mac, Windows o Linux) a otro. Puede parecer complicado, pero los servidores del FTP son simplemente computadoras que tienen una dirección del FTP y se dedican a recibir conexiones del FTP. Realizan dos simples tareas: “obtener” y “poner”."_
[¿Qué es FTP?](https://experience.dropbox.com/es-la/resources/what-is-ftp)
<br>
Nuevamente abrimos nuestro **Administrador del Servidor**, estando en este nos dirigimos a la barra de navegación y desplegamos el menú de la pestaña **Administrar**. Elegimos **Agregar roles y caracteristicas**.
![](./img/prev/5.png)
Dentro del apartado de **Servidor IIS** encontramos el **Servidor FTP**, lo seleccionamos.
![](./img/ftp/1.png)
Luego en la pestaña de **Herramientas** del Administrador del Servidor, elegimos la opción de **Usuarios y equipos de Active Directory**
![](./img/ftp/2.png)
Creamos una **Unidad organizativa**
![](./img/ftp/3.png)
La nombramos FTP
![](./img/ftp/4.png)
Ya dentro de esta podemos crear usuarios
![](./img/ftp/5.png)
Especificamos un nombre de pila y de inicio de sesión de usuario
![](./img/ftp/6.png)
Podemos elegir, de acuerdo a una contraseña ingresada, si esta nunca expirará, si el usuario nunca la puede cambiar, si el usuario cambia la contraseña en el siguiente inicio de sesión o si deshabilitamos directamente la cuenta.
![](./img/ftp/7.png)
Podemos ver los usuarios creados
![](./img/ftp/8.png)
Creamos un grupo en el cual podemos agregar a los usuarios que queramos de los que acabamos de crear
![](./img/ftp/9.png)
Podemos agrager más o quitar cuando queramos.
![](./img/ftp/10.png)

En la carpeta **inetpub** del disco local, creamos una carpeta, y a esta le editamos los permisos, de tal forma que solo los usuarios o grupos que especifiquemos puedan interactuar con esta.
![](./img/ftp/11.png)
En las propiedades de la carpeta, en la pestaña de seguridad, vamos a **Opciones avanzadas**
![](./img/ftp/12.png)
Damos en **Deshabilitar herencia**
![](./img/ftp/13.png)
Seleccionamos la opción de **Convertir los permisos heredados en permisos explicitos en este objeto**
![](./img/ftp/14.png)
Damos **Aceptar**. Ya devuelta a este menú hacemos click en **Editar**
![](./img/ftp/12.png)
Agregamos el grupo previamente creado
![](./img/ftp/15.png)
Desde el Administrador de IIS seleccionamos **Agregar sitio FTP**
![](./img/ftp/16.png)
Le damos un nombre y le indicamos la ruta de la carpeta a la que previamente le habiamos modificado el acceso
![](./img/ftp/17.png)
Especificamos nuestra IP **192.168.17.2**, además del puerto que siempre se maneja para FTP **21**. Aunque recomendado, de momento no usaremos **SSL**
![](./img/ftp/18.png)
Indicamos **Autenticación básica**, en **Autorización** le permitimos el acceso solamente a **Roles o grupos de usuarios especificados**, seguido a eso colocamos el nombre del grupo en este caso **GrupoFTP** con permisos de lectura.
![](./img/ftp/19.png)