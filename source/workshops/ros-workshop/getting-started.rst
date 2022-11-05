.. This document walks through the basic steps to getting the VM installed and configured

Getting Started
===============

To follow along with this workshop, you will want to download Visual Studio Code (VS Code) and  that has been developed for the workshop.


Prerequisites
-------------
Before starting this guide, make sure you have the following things installed:

:download:`VS Code <https://code.visualstudio.com/Download>`

:download:`Docker Desktop <https://www.docker.com/products/docker-desktop>`

:download:`WSL2 Kernel Update (if necessary) <https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi>`

Create A Folder
---------------
Create a folder titled *ros-workshop*, which will store the code for this workshop.

Starting Our Terminal Windows for Docker
----------------------------------------
To start, open **Visual Studio Code** and open the "ros-workshop" folder you created.
Next, Open the *ros-workshop* folder in VS Code, then select Terminal -> New Terminal.
Finally, click the Split Terminal option twice, which will give you three terminal windows.

Starting and Entering our Docker Container
------------------------------------------
For the first terminal, start the container with:

.. code:: powershell

    docker run -it -v ${PWD}:/ros-workshop --name ros-workshop ros:humble
    
For the other two, and for all subsequent containers, run:

.. code:: powershell

    docker exec -it ros-workshop bash
    source "/opt/ros/$ROS_DISTRO/setup.bash"