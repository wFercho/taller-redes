## Servidor DNS
_"Los servidores DNS convierten las solicitudes de nombres en direcciones IP, con lo que se controla a qué servidor se dirigirá un usuario final cuando escriba un nombre de dominio en su navegador web. Estas solicitudes se denominan consultas."_
[¿Qué es DNS?](https://aws.amazon.com/es/route53/what-is-dns/#:~:text=Los%20servidores%20DNS%20convierten%20las,Estas%20solicitudes%20se%20denominan%20consultas.)
<br>
Si hasta el momento todo se ha seguido en orden, en el proceso de instalación del Active Directory se tuvo que haber instalado DNS, por lo que solo tendríamos que configurarlo.  

Ingresamos al **Administrador de DNS**
![](./img/dns/1.png)
En el menú lateral ingresamos a **Zonas de busqueda directa**, ingresamos a nuestro dominio y seleccionamos la opción de **Host Nuevo**
![](./img/dns/2.png)
Especificamos un nombre la dirección IP **192.168.17.2**
![](./img/dns/3.png)
Posteriormente en **Zonas de busqueda inversa** vamos a **Zona nueva**
![](./img/dns/4.png)
En el **Asistente para nueva zona** avanceremos con lo que nos da por defecto
![](./img/dns/5.png)
![](./img/dns/6.png)
![](./img/dns/7.png)
![](./img/dns/8.png)
Acá especificamos los tres primeros octetos de nuestra dirección IP **192.168.17.**
![](./img/dns/9.png)
En esta parte es importante seleccionar **No adminitr actualizaciones dinámicas**, ya que como colocamos la dirección IP de forma estatica al servidor DNS no queremos que esta cambie.
![](./img/dns/10.png)
Ya con esto finalizamos.
![](./img/dns/11.png)
Seleccionamos la zona que acabamos de crear y seleccionamos **Nuevo Puntero (PTR)**
![](./img/dns/12.png)
Seleccionamos el host previamente creado
![](./img/dns/13.png)
Comprobamos que todo esté en orden, y damos **Aceptar**.
![](./img/dns/14.png)