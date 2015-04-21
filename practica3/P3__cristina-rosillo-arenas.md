#Práctica 3

**Instalación y configuración de Nginx en la máquina Balanceador

Realizamos la instalación siguiendo las instrucciones descritas en el guión de prácticas. Una vez instalado nginx, 
editaremos el fichero de configuración.

![captura1_0](http://i.imgur.com/lA5hGZD.png)

A continuación reiniciaremos nginx y comprobaremos que reparte las peticiones de forma equitativa.

![captura1_1](http://i.imgur.com/DlnWkpT.png)

Ahora se ha configurado para que la máquina 1 acepte dos peticiones por cada una que acepte la máquina 0.

![captura1_2](http://i.imgur.com/xGdl1jF.png)

Y por último hemos realizado un balanceo por IP, de forma que un servidor siempre reciba la peticiones de
una misma IP.

![captura1_3](http://i.imgur.com/BVweKIU.png)

**Instalación y configuración de Haproxy en la máquina Balanceador

Lo primero que haremos será parar el servicio de Nginx para que no interfieracon Haproxy.
Instalaremos Haproxy siguiendo las instrucciones que se dan en el guión de prácticas. Como hicimos anteriormente,
una vez instalado, editaremos el fichero de configuración.

![captura2_1](http://i.imgur.com/AZyxthD.png)

Una vez configurado, arrancamos el servicio y comprobamos que al igual que en el caso anterior el balanceador
reparte las peticiones de forma equitativa.

![captura2_2](http://i.imgur.com/DlnWkpT.png)
