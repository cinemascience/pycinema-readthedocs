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

Getting Started
---------------

Download the `example data repository. <https://github.com/cinemascience/pycinema-examples/archive/refs/tags/v3.0.zip>`_

The `cinema` command line tool can view databases using a set of `application` released with the module. Currently, there are `view` and `explore` application, and they are called on specific databases in the following way:

.. code-block:: console

   cinema view data/sphere.cdb

.. image:: img/cinema-view-sphere.png
   :align: center

Likewise, the `explore` application can be used to view the sample database:

.. code-block:: console

   cinema explore data/sphere.cdb

.. image:: img/cinema-explorer-sphere.png
   :align: center

The main difference between the two application is that `explore` uses a parallel coordinates widget to explore metadata, while the `view` application uses a set of sliders.

Building a Filter Graph
-----------------------

One of the most powerful capabilities of `pycinema` is support for building new filter graphs, specific to a task. It's easy to 
connect filters together, adjust views, and create visual layouts of information that help you look at complex data.

To get started, run the cinema application from the command line, and the `Cinema:Theater` application will open and you will see 
a blank window, which is the node layout window:

.. code-block:: console

   cinema view data/sphere.cdb

.. image:: img/build_01.png
   :align: center

First, add a filter to read in some data. Click on the **Edit** menu item, and choose the **Add filter ...** item. The filter selection window will appear. Diuble clicking on a name in the scroll box will create a node in the canvas. 

.. image:: img/filter_menu.png
   :align: center

Components of a single filter UI
--------------------------------

Each filter will have places that can accept input (like a text box), and dots showing places that can be connected (either inputs or outputs. In this example, we see the inputs and outputs of a *CinemaDatabaseReader* filter:

- **table** is an output connection
- **path** is an attribute describing the path to the database
- **file_column** is an attribute describing the column in the Cinema database that contains the file path for the artifact.

.. image:: img/build_02.png
   :align: center

Connecting filters
------------------

.. image:: img/build_03.png
   :align: center

.. image:: img/build_04.png
   :align: center

.. image:: img/build_05.png
   :align: center


