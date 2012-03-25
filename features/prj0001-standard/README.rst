=================================================
Crear el manual el Proyecto Standard de Eneboo
=================================================

    Nota: Este documento está en proceso de desarrollo.

El proyecto Standard_ de Eneboo_ (en adelante *Eneboo Standard*) es una compilación de módulos y extensiones de Eneboo que pretende cubrir las necesidades básicas de gestión de la mayoría de las empresas pequeñas y los autónomos.

Este documento detalla las convenciones establecidas para crear el manual del proyecto Standard de Eneboo. Es una guía rápida de uso de reStructuredText_ y Sphinx_, una selección de funciones y directivas de estos lenguajes que se usarán para crear el manual. Para profundizar más en las posibilidades de ambos se debe consultar sus respectivos sitios web.


El lenguaje elegido
------------------------

Se usará el lenguaje de marcas reStructuredText_. Para la generación de índices y la creación automática de ficheros HTML y LaTeX, se usará Sphinx_.

La tabla de contenidos
--------------------------

El *toctree*, "table of contents tree", es un índice que apunta a los distintos capítulos del manual. Sphinx_ utilizará este fichero para crear el índice en HTML o LaTeX. Para modificarlo hay que editar el fichero ``index.rst`` y modificar las opciones de la directiva *toctree*::

    .. toctree::
        :maxdepth: 2
   
        introduccion
        instalacion
        config

La lista de nombres que aparecen debajo de *:maxdepth: 2* corresponden a ficheros que contienen la documentación de cada uno de los capítulos del manual. Todos estos ficheros deben tener sufijo ``.rst`` y estar escritos en lenguaje reStructuredText_, aunque el sufijo ``.rst`` NO debe incluirse en la lista de la directiva *toctree*.

En resumen, para añadir capítulos al índice basta con incluir el nombre del fichero sin el sufijo ``.rst`` en la lista de la directiva *toctree* del fichero ``index.rst``.


Los capítulos
-------------------

Como se ha dicho en el punto anterior, cada capítulo del manual se guardará en un fichero ``.rst`` distinto.


Formateando el texto
----------------------

A continuación se detalla el subconjunto de marcas de reStructuredText_ que se usará para formatear el texto:

**El título del capítulo** debe aparecer al principio de cada fichero de capítulo. Por encima y por debajo de éste se debe incluir una línea de símbolos de igual (\=) de la siguiente forma::

    ===========================================
    Primeros pasos
    ===========================================
        
**Las secciones**, es decir, los distintos apartados de cada capítulo, tendrán debajo del texto una línea de guiones (\-), como por ejemplo::
    
    Editar líneas de una factura
    -------------------------------

**Los elementos propios de la aplicación**, como nombres de campos o botones, deberán ir *en cursiva* para distinguirlos mejor. Para hacer esto, se pondrán entre dobles asteriscos, como se puede ver a continuación::
    
    Para crear una nueva factura pulse el botón \*Insertar registro*.
        
Enlaces
------------------

**Enlaces internos**
    
Para incluir un enlace a un capítulo
    
**Enlaces externos**
      
Para incluir un enlace a una URL externa a la documentación, el texto del enlace debe ir seguido de un guión bajo (\_). Si el enlace está compuesto de más de una palabra, todo el texto debe ir entre comillas simples. Al final del documento, se definirán todas las URL externas del documento. Véase el siguiente ejemplo::
      
    Eneboo_ es `software libre`_ de tipo ERP_.
        
    ...
    ...
    ...
        
    .. _Eneboo: http://www.eneboo.org
    .. _`software libre` http://es.wikipedia.org/wiki/Software_libre
    .. _ERP http://es.wikipedia.org/wiki/Planificaci%C3%B3n_de_recursos_empresariales

.. _reStructuredText: http://docutils.sf.net/rst.html
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
.. _Eneboo: http://www.eneboo.org
.. _Standard: https://github.com/gestiweb/eneboo-features/tree/master/prj0001-standard
