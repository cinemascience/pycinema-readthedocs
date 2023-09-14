Usage
=====

.. _installation:

Installation
------------

To use `pycinema`, first install it using pip:

.. code-block:: console

   (.venv) $ pip install pycinema 

This will install the pycinema module, which includes both the filter library and the `cinema` command line tool.
The `pycinema` module will be available in normal python scripts, and the `cinema` command line tool will be
available in your shells. 

Getting Started
---------------

The `cinema` command line tool can view databases using a set of `workspaces` included with the application. Currently, there are `view` and `explorer` workspaces, and they are called on specific databases in the following way:

.. code-block:: console

   cinema view data/sphere.cdb

.. image img/cinema-view-sphere.png

Likewise, the `explorer` workspace can be used to view the sample database:

.. code-block:: console

   cinema view data/sphere.cdb

.. image img/cinema-explorer-sphere.png
