======================================
Documentar Extensiones Lab en Eneboo
======================================

El eneboo-lab_ es un repositorio de extensiones en proceso de desarrollo que todavía no han pasado al repositorio oficial eneboo-features_.

Este documento detalla las convenciones establecidas para documentar las extensiones de eneboo-lab_.

El lenguaje elegido
------------------------
Se usará el lenguaje de marcas reStructuredText_, ya que GitHub lo interpreta y muestra formateado. Así, podemos documentar directamente en el repositorio.

Una vez que la extensión pasa a formar parte de eneboo-features_, las convenciones para su documentación varían ligeramente para que la documentación generada se pueda combinar con Sphinx_. Estas convenciones pueden consultarse en https://github.com/gestiweb/eneboo-doc/blob/master/features/README.rst

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

    
Descripción de la funcionalidad
    En varios párrafos se describirán las nuevas funcionalidades que
    esta extensión aporta a un proyecto. Se usará texto en **cursiva** (entre \*\*dobles
    asteriscos\*\*) para los elementos de Eneboo como campos de datos, títulos de
    formularios, etc.
    
Capturas de pantalla
    Bajo ese título se mostrarán imágenes de las capturas de pantalla más descriptivas
    del funcionamiento de la extensión. Se usará la directiva figure_ de la siguiente
    forma::
    
        .. figure:: /gestiweb/eneboo-features/blob/master/ext0015-subfamilia/doc/edicion_articulo.png?raw=true
           :width: 500 px
           
           Descripción de la captura.
           
    Se debe procurar que el nombre del fichero de la captura sea descriptivo.
    Las rutas de las imágenes deben ser como la que aparece en el ejemplo si queremos que se vean bien en GitHub, ya que esta plataforma no encuentra las imágenes con rutas como ``doc/master_citas.png``.

Ejemplo
------------------------
    
Sirva como ejemplo la documentación de la extensión **agenda** que se puede ver en https://github.com/rmenor/eneboo-lab/tree/master/agenda


.. _reStructuredText: http://docutils.sf.net/rst.html
.. _figure: http://docutils.sourceforge.net/docs/ref/rst/directives.html#figure
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
.. _eneboo-lab: https://github.com/rmenor/eneboo-lab
.. _eneboo-features: https://github.com/gestiweb/eneboo-features
