.. This document outlines the ros2 run command, and how it can be used to launch nodes

ros2 run
========

This command is used to run nodes within a package, by activating certain entrypoints within the package definition.

Usage
-----

.. code:: bash

    ros2 run [PACKAGE] [EXECUTABLE]

:[PACKAGE]:

    This is replaced with the `packge` that the code is located within. The `packge` is the highest level folder underneath the `src` folder.


:[EXECUTABLE]:

    This is replaced with the `executable` name located in the `setup.py` file. This can be used to trigger specific files within a node.