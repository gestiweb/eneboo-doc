Instalar manualmente el programa desde tar.gz
=================================================

En la zona de descargas proporcionamos dos tipos de compilaciones, los tar.bz2 
y los paquetes para cada sistema operativo.

Actualmente sólo proveemos paquete para Windows 32 bits y compilaciones para 
Linux y Windows de 32 bits. Si tiene algún otro sistema operativo, puede echar 
un vistazo al listado completo de descargas: 

http://www.eneboo.com/pub/eneboo/builds/v2.4.0/


Instalar paquetes para Windows
--------------------------------------------------------------------

Los paquetes para Windows vienen en forma de instalador ejecutable. Tan sólo 
hay que seguir los pasos del instalador. Por defecto se instala en 
C:\Archivos de Programa\eneboo-2.4 y deja accesos directos en el menu inicio 
bajo la carpeta "Eneboo".


Instalar desde compilación en .tar.bz2
--------------------------------------------------------------------

Los ficheros .tar.bz2 son ficheros comprimidos que traen el resultado de la 
compilación y son "programas portables", es decir, pueden ser ejecutados sin 
ninguna instalación. Son ideales para introducirlos en un pendirve y 
ejecutarlos en cualquier ordenador, sin necesidad de instalar.

En Windows, un buen programa para descomprimir estos ficheros puede ser 7-Zip, 
aunque también sirven WinRAR y muchos otros.

En Linux y otros sistemas Unix, es necesario tener instalado la utilidad "tar" 
y "bzip2". Estas utilidades están instaladas por defecto en prácticamente todas 
las distribuciones. La mayoría incluso incorpora utilidades gráficas para 
descomprimir estos ficheros. Si quiere descomprimirlos usando la consola 
(porque carece de programa gráfico) puede intentar lo siguiente::

    tar jxf eneboo-v2.4.0-alpha3-linux32.tar.bz2

Si desea instalarlo a nivel de sistema, deberá copiarlo manualmente a las 
carpetas correspondientes y crearse los accesos directos 
que considere necesarios.

El proceso para instalación manual en Windows es el siguiente:

Copie el contenido de la carpeta eneboo-2.4-xxxx a C:\Archivos de programa\eneboo-2.4

Cree un acceso directo a la aplicación bin/eneboo  en el menú inicio->programas
 
El proceso para instalación manual en Linux es el siguiente: (necesitará permisos de superusuario)

Copie el contenido de la carpeta eneboo-2.4-xxxx a /opt/eneboo-2.4::

    $ sudo cp -R eneboo-2.4-xxxx /opt/eneboo-2.4

Cree un enlace simbólico de /opt/eneboo-2.4/bin/eneboo a /usr/local/bin/eneboo::

    $ sudo ln -s /opt/eneboo-2.4/bin/eneboo a /usr/local/bin/eneboo

Cree manualmente un acceso directo en su menú de programas a 
/usr/local/bin/eneboo. La iconografía del programa la podrá encontrar 
en /opt/eneboo-2.4/share/eneboo/images