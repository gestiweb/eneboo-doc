===============================================
Cómo colaborar en la edición de este manual
===============================================

Este manual está siendo desarrollado por la Comunidad Eneboo. Si estás interesado en colaborar con la creación del mismo, en este capítulo puedes encontrar cómo hacerlo.


Descargar los fuentes
---------------------------

Los fuentes del manual de Eneboo Standard se encuentran en un repositorio_ en GitHub. Si deseas colaborar con la edición del manual deberás darte de alta en GitHub y crear un fork. Si no estás familiarizado con GitHub, necesitarás aprender algunas `nociones básicas`_ para obtener documentación y subir cambios.


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

Como se ha dicho en el punto anterior, cada capítulo del manual se guardará en un fichero ``.rst`` distinto. Para editar un capítulo hay que editar el fichero asociado en cualquier editor de texto.


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
        

**Enlaces dentro del manual**
Para crear un enlace a, por ejemplo, otra sección del manual, se utiliza la directiva *ref* de la siguiente forma::

    El manual se encuentra en proceso de desarrollo, por lo que algunas partes pueden aparecer incompletas. Si desea
    colaborar en su edición vea :doc:`aquí<como_colaborar>` cómo hacerlo.


**Enlaces externos**
      
Para incluir un enlace a una URL externa a la documentación, el texto del enlace debe ir seguido de un guión bajo (\_). Si el texto del enlace está compuesto de más de una palabra, todo el texto debe ir entre tildes (\`). Al final del documento, se definirán todas las URL externas del documento como puede verse en el siguiente ejemplo::
      
    Eneboo_ es `software libre`_ de tipo ERP_.
        
    ...
    ...
    ...
        
    .. _Eneboo: http://www.eneboo.org
    .. _`software libre`: http://es.wikipedia.org/wiki/Software_libre
    .. _ERP: http://es.wikipedia.org/wiki/Planificaci%C3%B3n_de_recursos_empresariales

** Incluir imágenes **

Se usará la directiva figure_ de la siguiente forma::
    
        .. figure:: images/eneboo_ejemplo.png
           :width: 480 px
           :height: 345 px
           
           Descripción de la imagen.

La imagen del ejemplo se verá así:

.. figure:: images/eneboo_ejemplo.png
   :width: 480 px
   :height: 345 px
   
   Descripción de la imagen.



Generar HTML
-------------------

Para generar los ficheros HTML hay que situarse en el directorio raíz de la documentación de Eneboo (donde se encuentra el fichero ``Makefile`` y ejecutar la siguiente instrucción::

    $ make html

Los ficheros HTML se generan en el directorio ``build``.



Recursos adicionales
------------------------

Como guía de para la creación de este manual se puede usar este :download:`manual <downloads/manual_isolix.pdf>` escrito por Isolix_. Aunque el manual de Isolix no se refiere a Eneboo Standard, corresponde a un proyecto Eneboo que comparte con Eneboo Standard muchas extensiones y módulos, por lo que puede resultar muy útil para nuestra tarea.


.. _repositorio: https://github.com/dezetage/eneboo-doc/tree/master/features/prj0001-standard
.. _reStructuredText: http://docutils.sf.net/rst.html
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
.. _Eneboo: http://www.eneboo.org
.. _Standard: https://github.com/gestiweb/eneboo-features/tree/master/prj0001-standard
.. _figure: http://docutils.sourceforge.net/docs/ref/rst/directives.html#figure
.. _Isolix: http://www.isolix.es
.. _`nociones básicas`: http://help.github.com/
