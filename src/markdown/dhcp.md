## Servidor DHCP
_"Cada dispositivo de una red basada en TCP/IP debe tener una dirección IP de unidifusión única para acceder a la red y sus recursos. Sin DHCP, las direcciones IP de los equipos nuevos o de los equipos que se mueven de una subred a otra deben configurarse manualmente, mientras que las direcciones IP de los equipos que se quitan de la red deben recuperarse manualmente"._

_"Con DHCP, todo este proceso está automatizado y se administra de forma centralizada. El servidor DHCP mantiene un grupo de direcciones IP y concede una dirección a cualquier cliente habilitado para DHCP cuando se inicia en la red. Dado que las direcciones IP son dinámicas (concedidas) en lugar de estáticas (asignadas permanentemente), las direcciones que ya no están en uso se devuelven automáticamente al grupo para la reasignación"._

[Articulo de Microsoft](https://learn.microsoft.com/es-es/windows-server/networking/technologies/dhcp/dhcp-top)
<br>
Nuevamente abrimos nuestro **Administrador del Servidor**, estando en este nos dirigimos a la barra de navegación y desplegamos el menú de la pestaña **Administrar**. Elegimos **Agregar roles y caracteristicas**.
![](./img/prev/5.png)
Seleccionamos **Servidor DHCP**
![](./img/dhcp/1.png)
Agregamos las caracteristicas adicionales
![](./img/dhcp/2.png)
Una vez finalizada la instalación, damos click en **Completar configuración de DHCP**
![](./img/dhcp/3.png)
Estando en el *Asistente posterior a la instalación de DHCP* damos **Siguiente**
![](./img/dhcp/4.png)
En la pestaña de **Autorización** verificamos que se haga referencia al usuario administrador y damos en **Confirmar**
![](./img/dhcp/5.png)
Ahora nos dirigimos al **Administrador de DHCP**, y en la pestaña de **IPv4** creamos un **Ámbito nuevo**
![](./img/dhcp/6.png)
En el **Asistente para ámbito nuevo** especificamos un nombre y una descripción a este.
![](./img/dhcp/7.png)
Ingresamos el intervalo de direcciones del ámbito, desde **192.168.17.100** hasta **192.168.17.254**
![](./img/dhcp/8.png)
Dejamos la **Duración de la concesión** por defecto, que son 8 días.
![](./img/dhcp/9.png)
Ingresamos la IP de puerta de enlace que previamente habiamos definido **192.168.17.1**
![](./img/dhcp/10.png)
Verificamos el dominio y la IP a la que hace referencia.
![](./img/dhcp/11.png)
Ya con eso podemos finalizar.