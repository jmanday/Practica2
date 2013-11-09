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

