=============================
Primeros pasos
=============================

Instalación
-------------------

Instalador automático
""""""""""""""""""""""""""

Este `instalador <http://www.eneboo.com/pub/contrib/eneboo-2.4-alpha5-standard-win32-installer.exe>`_ permite que en pocos minutos Eneboo Standard esté listo para trabajar. El instalador realiza las siguientes tareas de forma automática:

    * Instala el motor de Eneboo.
    * Instala el gestor de bases de datos PostgreSQL con la configuración por defecto.
    * Carga los módulos y extensiones del proyecto Eneboo Standard.
    
De momento sólo está disponible para Windows.

Instalación manual
"""""""""""""""""""""""""

**Macintosh**

    #. Descargar y descomprimir el `motor de Eneboo para Mac OS X <http://eneboo.com/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0-alpha5-mac32.zip>`_ (sólo para 32 bits).
    #. Descargar e instalar el gestor de bases de datos PostgreSQL (recomendamos la versión 8.4) para Mac del `área de descarga de PostgreSQL`_. La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
    #. Descargar el `paquete de Eneboo Standard`_.
    #. `Cargar el paquete de Eneboo Standard`_.
    
**Linux**

    #. Descargar y descomprimir el motor de Eneboo para Linux de `32 bits <http://eneboo.com/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0-alpha5-linux32.tar.bz2>`_ o de `64 bits <http://www.eneboo.com/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0-alpha5-preview2-linux64.tar.bz2>`_ según necesitemos. El ejecutable está en ``eneboo-v2.4.0-alpha5/bin/eneboo``. Aunque el programa desde directorio, se recomienda moverlo a las rutas habituales de instalación de software como /opt/.
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



.. _`área de descarga de PostgreSQL`: http://www.enterprisedb.com/products-services-training/pgdownload
.. _`paquete de Eneboo Standard`: http://eneboo.com/pub/eneboo/modules/standard.eneboopkg
