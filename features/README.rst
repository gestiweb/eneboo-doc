==================================
Documentar Extensiones en Eneboo
==================================

Este documento detalla las convenciones establecidas para documentar las extensiones de Eneboo.

El lenguaje elegido
------------------------
Se usará el lenguaje de marcas reStructuredText_ ya que sus características permiten varios usos:
#. La documentación se podrá consultar directamente en GitHub, ya que esta plataforma interpreta código RST.
#. Usando `Sphinx <http://sphinx.pocoo.org/genindex.html>` y las plantillas adecuadas, se podrá generar una documentación en HTML con un diseño más acorde con la imagen del proyecto Eneboo.
#. Usando Sphinx también se podrá generar documentación en PDF pasando por LaTeX.

Ficheros y carpetas usados
------------------------------
Dentro del directorio de cada extensión se creará:
- Un fichero :file:`README.rst`. Este fichero de texto describirá el funcionamiento de la extensión.
- Un directorio :file:`images`. Este directorio contendrá algunas capturas de pantalla con las que ilustrar el funcionamiento de la extensión.

Estructura del fichero README.rst
---------------------------------------

.. rst:role:: Nombre de la extensión
    Es el valor del campo ``description`` en el fichero :file:`.feature.ini`.
    Inicialmente se puede escribir, aunque lo ideal sería leerlo de ese fichero para
    incluirlo en la documentación de forma automática.
    Para que aparezca como título, se escribirán encima y debajo del nombre sendas
    líneas con el símbolo ``=``.
    
.. rst:role:: Descripción de la funcionalidad
    En los párrafos que sean necesarios se describirán las nuevas funcionalidades que
    esta extensión aporta a Eneboo. Se usará texto en **cursiva** (entre dobles
    asteriscos) para los elementos de Eneboo como campos de datos, títulos de
    formularios, etc.
    
.. rst:role:: Capturas de pantalla
    Bajo ese título se mostrarán imágenes de las capturas de pantalla más descriptivas
    del funcionamiento de la extensión. Se usará la directiva figure_ de la siguiente
    forma::
    
        .. figure:: captura1.jpg
           :height:300px
           :width: 400 px
           
           Descripción de la captura.
           

    
Sirva como ejemplo la documentación de la extensión 0015-subfamilias


.. _reStructuredText: http://docutils.sf.net/rst.html
.. _figure: http://docutils.sourceforge.net/docs/ref/rst/directives.html#figure
