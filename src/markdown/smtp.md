## Servidor SMTP
_"Un servidor SMTP, también conocido como servidor de correo saliente, es una computadora o un software que administra los mensajes del correo electrónico salientes. En general, un servidor de correo se refiere a un sistema que recopila, administra y envía correos electrónicos. Un servidor SMTP se refiere específicamente al componente del servidor de correo que utiliza el protocolo simple de transferencia de correo (SMTP) para enviar correos salientes. Mientras que el servidor de correo administra los correos electrónicos entrantes y salientes, el servidor SMTP se ocupa solo de enviar y retransmitir los correos electrónicos salientes a los destinos apropiados. También puede denominarse servidor de correo electrónico saliente"._
[¿Qué es SMTP?](https://aws.amazon.com/es/what-is/smtp/)
<br>
Nuevamente abrimos nuestro **Administrador del Servidor**, estando en este nos dirigimos a la barra de navegación y desplegamos el menú de la pestaña **Administrar**. Elegimos **Agregar roles y caracteristicas**.
![](./img/prev/5.png)
En la pestaña de **Caracteristicas** seleccionamos **Servidor SMTP**
![](./img/smtp/1.png)
Agregamos caracteristicas adicionales.
![](./img/smtp/2.png)
Finalizada la instalación nos dirigimos a **Herramientas** de la barra de navegación del **Administrador de Servidor** y seleccionamos **Administrador de Information Services (IIS) 6.0**
![](./img/smtp/3.png)
Nos vamos a **Servidor virtual SMTP...**
![](./img/smtp/4.png)
Le damos un nombre
![](./img/smtp/5.png)
Seleccionamos nuestr IP **192.168.17.2**
![](./img/smtp/6.png)
Le indicamos la ruta del directorio principal de subdirectorios para contenido SMTP
![](./img/smtp/7.png)
Ingresamos nuestro dominio
![](./img/smtp/8.png)
Como tenemos que gestionar el envio de correos por POP3, descargamos e instalamos **Visendo SMTP Extender Communnity**
![](./img/smtp/9.png)
Aceptamos terminos
![](./img/smtp/10.png)
Le damos un nombre y en **Organization** ingresamos nuestro dominio
![](./img/smtp/11.png)
Una vez instalado, podemos verificar que nuestra IP aparece asociada
![](./img/smtp/12.png)
Para crear una cuenta solo ingresamos una dirección de correo y una contraseña
![](./img/smtp/13.png)
En este panel podemos ver las cuentas creadas
![](./img/smtp/14.png)
Instalamos Foxmail
![](./img/smtp/15.png)
Cuando lo ejecutamos tenemos que elegir **Other MailBox**
![](./img/smtp/16.png)
Creamos una cuenta con nuestro dominio
![](./img/smtp/18.png)
![](./img/smtp/19.png)
