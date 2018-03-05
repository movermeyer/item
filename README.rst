====
item
====

.. image:: https://travis-ci.org/lorien/item.png?branch=master
    :target: https://travis-ci.org/lorien/item?branch=master

.. image:: https://coveralls.io/repos/lorien/item/badge.svg?branch=master
    :target: https://coveralls.io/r/lorien/item?branch=master

.. image:: https://img.shields.io/pypi/dm/item.svg
    :target: https://pypi.python.org/pypi/item

.. image:: https://img.shields.io/pypi/v/item.svg
    :target: https://pypi.python.org/pypi/item

.. image:: https://landscape.io/github/lorien/item/master/landscape.png
   :target: https://landscape.io/github/lorien/item/master


Usage Example
=============

.. code:: python

    from item import Item
    from lxml.html import fromstring

    class SomeStructure(Item):
        id = IntegerField('//path/to/@id')
        name = StringField('//path/to/name')
        date = DateTimeField('//path/to/@datetime', '%Y-%m-%d %H:%M:%S')

    structure = SomeStructure(fromstring(SOME_HTML))
    print(structure.id)
    print(structure.name)
    print(structure.date)


Installation
============

.. code:: bash

    pip install item
