.. This file outlines how to use the rosdep command

rosdep
======

`rosdep`, or the *ROS Dependency Manager*, is used to manage and make sure all dependencies needed within a workspace are properly installed.

.. warning::

    This command needs to be run from the **root of your workspace**, as it is used to update packages for all projects within a given workspace

Usage
-----

.. code:: bash

    rosdep install -i --from-path src --rosdistro foxy -y

