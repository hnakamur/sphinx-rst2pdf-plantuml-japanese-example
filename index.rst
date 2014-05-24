.. sphinx rst2pdf example documentation master file, created by
   sphinx-quickstart on Sat May 24 14:30:43 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to sphinx rst2pdf example's documentation!
==================================================

Contents:

こんにちは、sphinxで作ったサンプル文書です。

.. uml::

   Alice -> Bob: Hi!
   Alice <- Bob: How are you?

.. uml::

   class "This is my class" as class1 {
      +myMethods()
      -myMethods2()
      String name
   }
   class class2 as "It works this way too" <<Serializable>> {
      String name
   }

   class2 *-- "foo/dummy" : use

.. toctree::
   :maxdepth: 2



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

