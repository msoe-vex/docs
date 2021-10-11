Install ROS 2
=============

Install ROS 2 Base Packages
-------------------------------------

To install ROS 2, the first thing we need to do is add the ROS 2 apt repositories to our system. First, we authorize the ROS 2 GPG key

.. code:: bash

    sudo apt update && sudo apt install curl gnupg2 lsb-release
    sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg

Then, we add the ROS 2 repository to our sources list

.. code:: bash

    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

We then need to update the apt repository caches so that apt knows where to go to find the newly added ROS 2 packages

.. code:: bash

    sudo apt update

Finally, we install the ROS 2 base desktop packages

.. code:: bash

    sudo apt install ros-foxy-desktop

Setting up ROS 2
----------------

Once ROS 2 is installed, we will want to install and setup some extra tools which we will need.

The first tool is rosdep. rosdep is the package manager for ROS and allows us to manage and install dependencies.

First, we source the base ROS 2 environment. Get used to doing this as for most things to work we will need have the base environment sourced in addition to the environment of the of the project you are working on. 

.. code:: bash

    source /opt/ros/foxy/setup.bash


Since we will always want to have the base ROS 2 environment sourced, we'll go ahead and add this command to our `bash.rc` file. This will make it so that each time we open a terminal, bash automatically sources the base ROS 2 environment. 

.. code:: bash

    echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc


Then, install rosdep

.. code:: bash

    sudo apt install python3-rosdep

Set rosdep up with the following commands

.. code:: bash

    sudo rosdep init
    rosdep update

Now we will want to install colcon, which is the build tool used in ROS 2

.. code:: bash

    sudo apt install python3-colcon-common-extensions
