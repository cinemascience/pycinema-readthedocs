Usage
=====

.. _installation:

Installation
------------

To use `pycinema`, first install it using pip:

.. code-block:: console

   $ pip install pycinema 

This will install the pycinema module, which includes both the filter library and the `cinema` command line tool.
The `pycinema` module will be available in normal python scripts, and the `cinema` command line tool will be
available in your shells. 

*Example Data* Download example data referenced in this documentation `here <https://github.com/cinemascience/pycinema-examples/archive/refs/tags/v2.0.zip>`_

Getting Started
---------------

The `cinema` command line tool can view databases using a set of `workspaces` included with the application. Currently, there are `view` and `explorer` workspaces, and they are called on specific databases in the following way:

.. code-block:: console

   cinema view data/sphere.cdb

.. image:: img/cinema-view-sphere.png
   :align: center

Likewise, the `explorer` workspace can be used to view the sample database:

.. code-block:: console

   cinema explorer data/sphere.cdb

.. image:: img/cinema-explorer-sphere.png
   :align: center

The main difference between the two workspaces is that `explorer` uses a parallel coordinates widget to explore metadata, while the `view` workspace uses a set of sliders.
