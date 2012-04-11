==================================
Documentar Extensiones en Eneboo
==================================

    Nota: Esta documentación está pendiente de revisión.

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
    Es el valor del campo *description* en el fichero ``descripcion_extension.feature.ini``.
    Para que aparezca como título, se escribirá una línea encima y otra debajo del nombre con el símbolo '='.
            El valor del campo *description* se puede sacar del fichero de forma automática con Sphinx_, aunque no con reStructuredText_, por lo que inicialmente se pondrá a mano.

    
Descripción de la funcionalidad
    En varios párrafos se describirán las nuevas funcionalidades que
    esta extensión aporta a un proyecto. Se usará texto en **cursiva** (entre dobles
    asteriscos) para los elementos de Eneboo como campos de datos, títulos de
    formularios, etc.
    
Capturas de pantalla
    Bajo ese título se mostrarán imágenes de las capturas de pantalla más descriptivas
    del funcionamiento de la extensión. Se usará la directiva figure_ de la siguiente
    forma::
    
        .. figure:: /gestiweb/eneboo-features/blob/master/ext0015-subfamilia/doc/edicion_articulo.png?raw=true
           :width: 500 px
           
           Descripción de la captura.
           
    Se debe procurar que el nombre del fichero de la captura sea descriptivo.
    Las rutas de las imágenes deben ser como la que aparece en el ejemplo si queremos que se vean bien en GitHub, ya que esta plataforma no encuentra las imágenes con rutas como ``doc/edicion_articulo.png``.

Ejemplo
------------------------
    
Sirva como ejemplo la documentación de la extensión 0015-subfamilias que se puede ver en https://github.com/gestiweb/eneboo-features/tree/master/ext0015-subfamilia


.. _reStructuredText: http://docutils.sf.net/rst.html
.. _figure: http://docutils.sourceforge.net/docs/ref/rst/directives.html#figure
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
