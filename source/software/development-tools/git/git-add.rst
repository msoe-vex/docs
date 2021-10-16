.. This document walks through the git add command

git add
=======


Command Usage
-------------

.. code:: bash

    git add [ARGUMENT] [FILE]

**Required Arguments:**

:[FILE]:
    This is the file you want to add. This should be the same path that shows up when running ``git status``, without any quotes on the file path. This also supports wildcards, such as ``*`` for matching everything, and ``.`` for all files in the current directory.

**Optional Arguments:**

:-A:
    Add all files with changes. This replaces the file argument, and allows all files to be added. **NOTE:** Make sure you capitalize the argument - lowercase will not work!