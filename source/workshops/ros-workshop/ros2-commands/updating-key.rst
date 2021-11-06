.. This document walks through updating the GPG key used to pull from ROS repositories

Updating your ROS GPG Key
=========================

There was a recent incident in which the ROS GPG key expired, making it impossible for users to pull updates from ROS packages in Ubuntu.

**If you are having issues getting ROS packages**:

In ROS1, run the following command:

.. code:: bash

    curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

In ROS2, run the following command:

.. code:: bash

    sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg