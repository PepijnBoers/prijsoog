.. image:: https://raw.githubusercontent.com/PepijnBoers/prijsoog/master/assets/prijsoog.png
   :target: https://raw.githubusercontent.com/PepijnBoers/prijsoog/master/assets/prijsoog.png 
   :align: center
   :height: 200px

========
Prijsoog
========


.. image:: https://img.shields.io/pypi/v/prijsoog.svg
        :target: https://pypi.python.org/pypi/prijsoog

.. image:: https://codecov.io/gh/PepijnBoers/prijsoog/branch/master/graph/badge.svg?token=NN5DTM3M60
        :target: https://codecov.io/gh/PepijnBoers/prijsoog  

.. image:: https://readthedocs.org/projects/prijsoog/badge/?version=latest
        :target: https://pepijnboers.github.io/prijsoog/_build/html/index.html
        :alt: Documentation Status


*This is a simple hobby project which main focus is to get familiar with webscraping, Sphinx documentation and PyPi deployment. I do not take any responsibility for possible site bans due to excessive page requests.*

Prijsoog provides an easy-to-use api for retrieving product-price combinations for specific grocery items in Dutch supermarkets. You can pass a grocery-related query to Prijsoog's search functionality to obtain a supermarket-depended list of related grocery items. Prijsoog sends a GET request to a selected set of the biggest Dutch supermarkets, and retrieves the top N products most relevant for your query. **In order to assure fair use of their server capacity, Prijsoog's defaults to a delay time of 5 seconds between queries.**


Installation
------------
Install the latest version of Prijsoog via `Pypi <https://pypi.org//>`_:
::

        pip install prijsoog

Quick Demo
----------

See following example

.. code-block:: python

        import prijsoog

        # Show Albert Heijn results for "kiwi"
        AH = prijsoog.AhWatcher()
        products = AH.search("kiwi")
        print(products)

        # Show Jumbo results for "kiwi"
        Jumbo = prijsoog.JumboWatcher()
        products = Jumbo.search("kiwi")
        print(products)



* Free software: MIT license
* Documentation: https://prijsoog.readthedocs.io


Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
