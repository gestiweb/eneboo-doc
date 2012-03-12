============================================
Documentar el Proyecto Standard de Eneboo
============================================

    Nota: Esta documentación está en proceso de desarrollo.

El proyecto Standard de Eneboo_ (en adelante *Eneboo Standard*) pretende ser una compilación de módulos y extensiones que
proporcionen una funcionalidad básica de gestión a la una buena parte de las pequeñas y medianas empresas.

La documentación generada será un manual de usuario que explicará cómo trabajar con Eneboo Standard.

Este documento detalla las convenciones establecidas para documentar el proyecto Standard de Eneboo. Es una guía rápida de uso de reStructuredText_ y Sphinx_, una selección de funciones y directivas de estos lenguajes que se usarán para crear el manual de Eneboo Standard. Para profundizar más en las posibilidades de ambos consultar sus respectivos sitios web.


El lenguaje elegido
------------------------

Se usará el lenguaje de marcas reStructuredText_. Para la generación de índices y la creación automática de HTML y LaTeX, se usará Sphinx_.

La tabla de contenidos
--------------------------

El *toctree*, "table of contents tree", es un índice que apunta a los distintos capítulos del manual. Sphinx_ utilizará este fichero para crear el índice en HTML o LaTeX. Para modificarlo hay que editar el fichero ``index.rst`` y modificar las opciones de la directiva *toctree*::

    .. toctree::
        :maxdepth: 2
   
        introduccion
        instalacion
        config

Como se puede deducir de manera intuitiva, la lista de nombres que aparecen debajo de *:maxdepth: 2* corresponden a ficheros que contienen la documentación de cada uno de los capítulos del manual. Todos estos ficheros deben tener sufijo ``.rst`` y estar escritos en lenguaje reStructuredText_, aunque el sufijo NO debe incluirse en la lista de la directiva *toctree*.




.. _reStructuredText: http://docutils.sf.net/rst.html
.. _Sphinx: http://sphinx.pocoo.org/genindex.html
.. _Eneboo: http://www.eneboo.org
