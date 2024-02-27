Setting up Cinema
=================

Environment
-----------

**PYCINEMA_SCRIPTS_DIR** 

A user-defined location that ``cinema`` will search *first* for scripts
executed through command line keys. A *key* is a unique identifier used as
command line shorthand to locate and execute scripts. For example, a user can
create a script named ``newscript.py`` and place it in ``PYCINEMA_SCRIPTS_DIR``
and then enter the following on the command line:

.. code-block:: console

   $ cinema newscript some-database.cdb 


``cinema`` will then look for ``newscript.py`` first in ``PYCINEMA_SCRIPTS_DIR`` and then
in the module installation (meaning it is looking for scripts included in the release)
This allows the user to both access new scripts, and to override the behavior of 
scripts that are part of the release (though the latter is not encouraged ...)
