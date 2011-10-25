
Compilar el programa
=================================================

Para compilar es necesario hacerlo desde Linux, incluso para producir 
ejecutables para otras plataformas (Windows, MacOS). Teóricamente es posible 
compilar Eneboo desde Windows o desde MacOS, pero no se ha intentado aún, por 
lo que es muy probable que falle la compilación nativa en estos sistemas.

Si no tiene Linux, siempre puede instalar una máquina virtual con VirtualBox 
y instalar dentro una imagen. 

A continuación describimos el proceso: 
 

Paso 1 - Obteniendo el código fuente
--------------------------------------------------------------------

Recomendamos el uso de GIT para descargar los fuentes. En la mayoría de 
distribuciones GIT viene como paquete y se puede instalar sin problemas. En 
Debian y Ubuntu basta con teclear "sudo apt-get install git-core" desde la 
consola.

Si no desea usar GIT, desde la zona de descargas se suelen proveer paquetes de 
código fuente en tar.bz2, se pueden descargar igualmente. También, desde la 
web de github, es posible descargar el código en formato ZIP o Tar.gz.

Tenga en cuenta que la detección de la versión actualmente se realiza usando 
comandos de GIT, por lo que si no está usando GIT, el ejecutable no llevará 
incrustada una versión correcta.
 


Paso 2 - Requisitos de compilación
--------------------------------------------------------------------

Vamos a necesitar las utilidades make, gcc, g++ y otras básicas. En Debian y 
Ubuntu, están todas bajo el paquete "build-essential".

En los fuentes hemos agregado un fichero llamado "compile-dependencies".  Este 
fichero contiene todos los paquetes necesarios para compilar AbanQ, un nombre 
de paquete por línea. Los nombres de paquete corresponden a Debian Wheezy, 
por lo que en su distribución de linux puede que tengan otro nombre. 

Si va a compilar para Windows desde Linux, debe además instalar los paquetes 
que aparecen en "win32-compile-dependencies".

Para MacOSX es posible que se requieran otros paquetes adicionales. Actualmente 
no tenemos descrito aún el proceso de compilación cruzada para MacOSX.

 


Paso 3 - Compilar
--------------------------------------------------------------------

El código fuente viene con un script llamado "build.sh", que acepta una serie 
de opciones (no documentadas aún, se puede ver en el código fuente). Para 
compilar para cada sistema, hemos creado unos scripts que pasan las opciones 
adecuadas para el sistema en cuestión: build_linux32.sh, build_windows.sh ... 

Si lo desea, puede examinar uno de estos scripts y lanzar manualmente 
build.sh agregando o modificando los parámetros que crea conveniente.

Recomendamos encarecidamente compilar en una máquina que disponga al menos 
de 2Gb de RAM y 4 cores. Los scripts están optimizados para paralelizar la 
compilación tanto como sea posible en su máquina. El tiempo de compilación 
estimado para 4 cores + Hyperthreading es de 10 minutos para la versión de 
Linux y 40 para la de Windows.

Si compila para Linux en una distribución reciente, es posible que el 
ejecutable no funcione en distribuciones antiguas (de hace 5 años) por una 
incompatibilidad en la ABI. Sin embargo los ejecutables creados en SO antiguos 
sí funcionan en los nuevos. En nuestro caso compilamos desde Debian Lenny 
para Linux. (Es posible que el motivo sea un paquete libstdc++-xxx-dev 
demasiado nuevo)

La compilación para Windows puede fallar en distribuciones muy antiguas, en 
nuestro caso, compilamos desde Debian Wheezy para Windows. Además, la 
compilación para Windows puede llegar a fallar en el primer intento, y al 
lanzarse por segunda vez consecutiva funcionar. Esto es debido por un problema 
de dependencias en libqwt y sus plugins (llega a compilar antes el plugin que 
la librería). Aún no hemos podido corregir esto.

La compilación, una vez terminada, debe crear una carpeta llamada 
"eneboo-build-xxxx"  en la que debemos tener una versión compilada de 
Eneboo perfectamente funcional. Al copiar esta carpeta a otro equipo, debería 
funcionar sin problemas.


A.1 - Notas de compilación
--------------------------------------------------------------------

A partir de la versión alpha4 (pendiente aún de release), la compilación para 
Windows también funciona en Debian Lenny. 

Para compilar de 64bits a 32bits, a veces hay que enlazar libXft.so en 
algunos sistemas::

    ln -s /usr/lib32/libXft.so.2 /usr/lib32/libXft.so
 


A.2 - Actualizar el código y limpiar el directorio de trabajo
--------------------------------------------------------------------

Para actualizar el código fuente, basta con hacer "git pull" y volver a 
compilar de nuevo. Pero a menudo, con cambios en el sistema de compilación, 
o en ficheros que no tienen las dependencias bien controladas, es posible que 
el resultado de la compilación falle. En estos casos es necesario limpiar el 
contenido de la compilación anterior.



B.1 - Empaquetar en tar.bz2
--------------------------------------------------------------------

Aunque no es obligatorio, sí es más fácil llevarse las compilaciones a otro 
equipo usando un fichero comprimido en lugar de una carpeta. Es bastante 
sencillo de realizar, pero de todos modos, hemos provisto de unos scripts 
llamados export_linux32.sh, export_windows.sh, ... que automatizan la tarea 
y dejan el comprimido dentro de la carpeta export/.
 

B.2 - Empaquetar para Windows en formato Instalador EXE
--------------------------------------------------------------------

Estamos usando los instaladores de NSIS para crear estos ejecutables. Es un 
instalador muy sencillo, que copia los ficheros en la carpeta adecuada y deja 
unos accesos directos. Dentro del código fuente está el fichero "eneboo.nsi", 
que es la plantilla que usamos con NSIS para crear éstos instaladores. No 
tenemos aún nada que modifique el fichero NSIS según la versión, por lo 
que hay que modificar el fichero cada vez que se crea el instalador para 
introducir la versión a mano.

El instalador se crea desde Windows, a partir del tar.bz2 empaquetado. El 
proceso a grosso modo es el que sigue:

1. Descomprimimos el tar.bz2 en windows y renombramos la carpeta a "eneboo"

2. Localizamos en el código fuente original el fichero de licencia COPYING.txt 
y lo copiamos dentro de la carpeta "eneboo"

3. Emplazamos el script eneboo.nsi en la carpeta padre de "eneboo".

4. Compilamos el script con el NSIS

Con esto, debería crearnos el ejecutable con el nombre que se le haya 
especificado en el script.

