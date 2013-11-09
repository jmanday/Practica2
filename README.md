Practica2
=========

<pre>
Autor: Manuel Jesús García Manday
</pre>

En este documento expondré los pasos realizados y herramientas utilizadas para la realización de la segunda práctica de la asignatura.


<br>
<h3>En que consiste</h3>  
He realizado un formulario en python con una serie de campos obligatorios y una seria de validaciones sobre los mismos que se deden cumplir para 
que se pueda rellenar correctamente. Dicha aplicación se va a enjaular en una jaula chroot donde probaremos su funcionamiento.

<br>
<h3>Debootstrap</h3>
Es la herramienta que he utilizado para crearme un sistema Debian básico. El comando ejecutado con sus correspondientes opciones es el siguiente:
<pre>
sudo debootstrap --arch=amd64 saucy /home/jaulas/saucy/ http://archive.ubuntu.com/ubuntu
</pre>

![imagen23](https://github.com/jmanday/Imagenes/blob/master/imagen23.png?raw=true)

![imagen24](https://github.com/jmanday/Imagenes/blob/master/imagen24.png?raw=true)

Previamente me he creado el directorio **saucy** (aunque la propia instalación te lo crea), ya que el directorio **jaulas** lo tenía ya creado por la realización de los ejercicios sobre este tema.

<br>
<h3>Jaula chroot</h3>
Antes que nada tenemos que configurar nuestra jaula, primeramente montaremos /proc del anfitrión y luego copiando el archivo para las dns locales.

![imagen26](https://github.com/jmanday/Imagenes/blob/master/imagen26.png?raw=true)


Una vez instalado y configurado el sistema accedemos a el.

![imagen25](https://github.com/jmanday/Imagenes/blob/master/imagen25.png?raw=true)



Continuando con la configuración de la jaula procederemos a instalar los paquetes necesarios para que la aplicación pueda correr en este sistema mínimo. 
Para ello instalamos los paquetes python y python-web2py. 

El primero lo instalamos directamente desde el gestor de paquetes apt-get:

![imagen27](https://github.com/jmanday/Imagenes/blob/master/imagen27.png?raw=true)

Para el segundo no es posible realizar la misma acción debido a que apt-get no tiene el repositorio, por lo que instalamos el paquete git y lo descargamos 
de su repositorio de github:

![imagen29](https://github.com/jmanday/Imagenes/blob/master/imagen29.png?raw=true)


![imagen28](https://github.com/jmanday/Imagenes/blob/master/imagen28.png?raw=true)


Una vez que hemos clonado el repositorio de python-web2py en nuestro Debian mínimo pasamos a instalarlo:

![imagen30](https://github.com/jmanday/Imagenes/blob/master/imagen30.png?raw=true)

