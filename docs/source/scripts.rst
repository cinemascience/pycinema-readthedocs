Running Cinema scripts
======================

The `cinema` command line tool makes a host of pycinema capability available through the
command line. The `cinema` help message shows the list of subcommands available, and a
short description of their capabilities:

.. code-block:: console
   $ cinema --help 

   usage: cinema [-h] {compose,meta,browse,discover,explore,imagegrid,view,theater} ...

   Cinema command line tool

   positional arguments:
     {compose,meta,browse,discover,explore,imagegrid,view,theater}
                           Sub-commands
       compose             convert Cinema float (hdf5) images to .png
       meta                dump descriptive metadata about a cinema database
       browse              browse a cinema database
       discover            discover a cinema database
       explore             explore a cinema database
       imagegrid           imagegrid a cinema database
       view                view a cinema database
       theater             run a cinema script in theater

    options:
      -h, --help            show this help message and exit

The `cinema` command line tool runs pycinema-created python scripts using the `pycinema`
module. These scripts can be run from the command line by providing the path to
the script as a command line argument.

This example script loads a Cinema database, queries for a single image, then
applies an image border to that image. Both the original and the image with the
border are displayed side-by-side.

.. code-block:: console

   $ cinema theater examples/theater/ImageBorder.py 


.. image:: img/script-imageborder.png
   :align: center

This example script loads a Cinema database, queries for a single image, then
applies an image edge detection algorithm to that image. The result of that
edge detection is then composited onto the original image using a mask
composite operation.

.. code-block:: console

   $ cinema theater examples/theater/ImageEdgeDetection.py 

.. image:: img/script-imageedgedetection.png
   :align: center

Scripts with No GUI
------------------------------

Some `pycinema` scripts do not not include GUI elements, and can be run
with `python`, assuming that the `pycinema` module has been installed. 
These scripts execute `pycinema` scripts, producing intermediate data 
products, files, etc. as defined by the filters.

For example, the following script reads in a Cinema database, then writes out the
`data.csv` file as a new csv file, without requiring the GUI:


.. code-block:: console

   $ python examples/theater/TableWriteHeadlessExample.py



