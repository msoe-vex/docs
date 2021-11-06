.. This document outlines how to use the colcon command in ROS2

colcon
======

The `colcon` command is used to interact with the build system of our ROS packages. This needs to be executed at the **root of the workspace** (highest level), and will produce the following items after building:

* A **build** directory to store temporary files needed for creating output files
* An **install** directory to store the final output files
* A **log** directory to store logging information from the build process

Usage
-----

.. code:: bash

    colcon [task] [args]

Tasks:

:build:

    Build the current workspace. This produces the directories listed above, and **needs** to be run before attempting to run tests!

:test:

    Run tests in the current workspace.

Optional Arguments:

:--symlink-install:

    The `--symlink-install` command can be used to speed up installation by linking changes directly from source to install files