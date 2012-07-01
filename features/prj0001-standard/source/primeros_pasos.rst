=============================
Primeros pasos
=============================

Instalación
-------------------

Instalador automático
""""""""""""""""""""""""""

Este instalador permite que en pocos minutos Eneboo Standard esté listo para trabajar. El instalador realiza las siguientes tareas de forma automática:

    * Instala el motor de Eneboo.
    * Instala el gestor de bases de datos PostgreSQL con la configuración por defecto.
    * Carga los módulos y extensiones del proyecto Eneboo Standard.
    
Se puede descargar en el apartado `Versiones Estables`_ del área de descarga de Eneboo, a través del enlace *Windows Installer 32bits Quick*.

De momento sólo está disponible para Windows y Linux.

Instalación manual
"""""""""""""""""""""""""

**Macintosh**

    #. Descargar y descomprimir el `motor de Eneboo para Mac OS X <http://eneboo.com/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0-alpha5-mac32.zip>`_ (sólo para 32 bits).
    #. Descargar e instalar el gestor de bases de datos PostgreSQL (recomendamos la versión 8.4) para Mac del `área de descarga de PostgreSQL`_. La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
    #. Descargar el `paquete de Eneboo Standard`_.
    #. `Cargar el paquete de Eneboo Standard`_.
    
**Linux**

    #. Descargar y descomprimir el motor de Eneboo para Linux en el apartado `Versiones Estables`_. Podemos elegir entre las versiones Build y Quick, de 32 o 64 bits.
    #. Descargar e instalar el gestor de bases de datos PostgreSQL (recomendamos la versión 8.4) para Linux del `área de descarga de PostgreSQL`_. La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
    #. Descargar el `paquete de Eneboo Standard`_.
    #. `Cargar el paquete de Eneboo Standard`_.


Cargar el paquete de Eneboo Standard
"""""""""""""""""""""""""""""""""""""""""

    #. Abrir Eneboo. Aparecerá la pantalla *Conectar*.
    #. Rellenar los campos con los siguientes valores:
    
        * Base de datos: standard
        * Usuario: el administrador de la base de datos PostgreSQL.
        * Contraseña: la del administrador de la base de datos PosgtreSQL.
        
    #. Pulsar el botón de la flecha hacia la derecha *Más opciones*.
    #. Rellenar los campos de esta pantalla con los siguientes valores:
    
        * Controlador: PosgtreSQL
        * Servidor: localhost
        * Puerto: 5432
        
       .. figure:: images/conectar.png
           
           Pantalla *Conectar*
           
     5. Pulsar el botón *Conectar*. Se mostrará un mensaje con el texto *La base de datos standard no existe ¿Quiere crearla?*. Pulsar *Sí*.
     #. Se iniciará el programa y se mostrará el entorno Eneboo. En el área de *Módulos* de la parte izquierda, abrir la opción *Sistema -> Administración -> Cargar Paquete de módulos*.
     #. Localizar el archivo ``standard.eneboopkg`` y pulsar *Abrir*. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.


Configuración inicial
-----------------------


Entorno Eneboo
-------------------



Circuito de ventas
-------------------


Circuito de compras
---------------------



.. _`Versiones Estables`: http://www.eneboo.org/site/stable
.. _`área de descarga de PostgreSQL`: http://www.enterprisedb.com/products-services-training/pgdownload
.. _`paquete de Eneboo Standard`: http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg
