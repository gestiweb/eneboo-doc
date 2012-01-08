==================================
Documentar Extensiones en Eneboo
==================================

Este documento detalla las convenciones establecidas para documentar las extensiones de Eneboo.

El lenguaje elegido
------------------------
Se usará el lenguaje de marcas reStructuredText_, ya que sus características permiten varios usos:

#. La documentación se podrá consultar directamente en GitHub, ya que esta plataforma interpreta código reST.

#. Usando Sphinx_ y las plantillas adecuadas, se podrá generar una documentación en HTML con un diseño más acorde con la imagen del proyecto Eneboo.

#. Usando Sphinx_ también se podrá generar documentación en PDF pasando por LaTeX.

Ficheros y carpetas usados
------------------------------

Dentro del directorio de cada extensión se creará:

- Un fichero ``README.rst``. Describirá el funcionamiento de la extensión.

- Un directorio ``doc``. Además de otros ficheros, contendrá algunas capturas de pantalla con las que ilustrar el funcionamiento de la extensión.


Estructura del fichero README.rst
---------------------------------------

Nombre de la extensión
    Es el valor del campo *description* en el fichero
    ``descripcion_extension.feature.ini``.
        Inicialmente se puede escribir, aunque lo ideal sería leerlo de ese fichero para
        incluirlo en la documentación de forma automática.
        Para que aparezca como título, se escribirán encima y debajo del nombre sendas
        líneas con el símbolo ``=``.
    
Descripción de la funcionalidad
    En los párrafos que sean necesarios se describirán las nuevas funcionalidades que
    esta extensión aporta a Eneboo. Se usará texto en **cursiva** (entre dobles
    asteriscos) para los elementos de Eneboo como campos de datos, títulos de
    formularios, etc.
    
.. rst:role:: Capturas de pantalla

    Bajo ese título se mostrarán imágenes de las capturas de pantalla más descriptivas
    del funcionamiento de la extensión. Se usará la directiva figure_ de la siguiente
    forma::
    
        .. figure:: captura1.jpg
           :width: 400 px
           
           Descripción de la captura.
           


Ejemplo
------------------------
    
Sirva como ejemplo la documentación de la extensión 0015-subfamilias que se puede ver en https://github.com/dezetage/eneboo-features/tree/master/ext0015-subfamilia.


.. _reStructuredText: http://docutils.sf.net/rst.html
.. _figure: http://docutils.sourceforge.net/docs/ref/rst/directives.html#figure
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
