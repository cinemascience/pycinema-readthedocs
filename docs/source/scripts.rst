Running Cinema scripts
======================

The `cinema` command line tool runs valid python scripts using the `pycinema`
module. These scripts can be run from the command line by providing the path to
the script as a command line argument.

This example script loads a Cinema database, queries for a single image, then
applies an image border to that image. Both the original and the image with the
border are displayed side-by-side.

.. code-block:: console

   $ cinema examples/theater/ImageBorder.py 


.. image:: img/script-imageborder.png
   :align: center

This example script loads a Cinema database, queries for a single image, then
applies an image edge detection algorithm to that image. The result of that
edge detection is then composited onto the original image using a mask
composite operation.

.. code-block:: console

   $ cinema examples/theater/ImageEdgeDetection.py 

.. image:: img/script-imageedgedetection.png
   :align: center

Scripts with No GUI
-------------------

We note that `pycinema` filter graphs that do not include GUI elements can be run
with python, and they will execute as expected, producing intermediate data 
products, files, etc. as defined by the filters.

For example, the following script reads in a Cinema database, then writes out the
`data.csv` file as a new csv file, without requiring the GUI:


.. code-block:: console

   $ cinema examples/theater/TableWriteHeadlessExample.py



