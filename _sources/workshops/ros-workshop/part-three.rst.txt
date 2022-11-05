.. This document walks through part three of the ROS workshop - introducing 3D turtlebot and Gazebo

Part 3: Simulation
==================

Docker Setup
------------
Because we are in a Docker container on Windows, there are a few hoops we need to jump through in order to launch our simulation programs.

First, install VcXsrv:
 
:download:`VcXsrv <https://sourceforge.net/projects/vcxsrv/files/latest/download>`

Just click next through the prompts to install VcXsrv, though if Windows gives you a prompt about allowing network access, make sure to select **Domain, Private, and Public**.

A new icon should appear on the desktop titled `XLaunch`. Double click that and click next and finish through all the prompts.

In a Docker terminal, run:

.. code:: bash

    apt install ros-humble-turtlebot3-{gazebo,teleop}

In **each** Docker terminal, run:

.. code:: bash

    export DISPLAY=host.docker.internal:0 LIBGL_ALWAYS_INDIRECT=1

This will allow our Docker container to connect to VcXsrv in Windows.

You are now ready to start simulating a robot!

2D Simulation
-------------

2D Simulation is a great place to start exploring the turtlebot platform. 

Let's start by running the base `turtlesim` program to open our primary window.

.. code:: bash

    ros2 run turtlesim turtlesim_node

This should generate a window with a turtle in the center. In a second terminal, run the following command to start up a node to control the turtle:

.. code:: bash

    ros2 run turtlesim turtle_teleop_key

With this second terminal in focus, you should now be able to control the turtle using the arrow keys!

From here, we can also open the `rqt` utility to better understand our current ROS network. Within an unused terminal window, run the following command:

.. code:: bash

    rqt

3D Simulation
-------------

One of the largest features of ROS is it's ability to simulate and visualize 3D environments. This section will introduce some of the tools that allow for these features, and start to walk through the basics of how they work.

Opening the Simulator
---------------------
Let's open one of the tutorial worlds provided to us in Gazebo. To do so, run the following command in an unused terminal:

.. code:: bash

    gazebo --verbose /opt/ros/humble/share/gazebo_plugins/worlds/gazebo_ros_diff_drive_demo.world

Opening this up, we should see the Gazebo environment load in with a simple test robot. Explore some of the tools in the environment, and look around.

Since we know where the "world" file is that it's loading, let's take a look at it. Type the following command into a second unused terminal, to open up the world configuration:

.. code:: bash

    cat /opt/ros/humble/share/gazebo_plugins/worlds/gazebo_ros_diff_drive_demo.world

Looking around, everything is all defined in XML format. The entire robot and the surrounding world are all defined within this file, along with all the rigging to make the robot move. Astute observers may also notice the commands located at the top of the file. Let's try running one of them to control the robot.

In a third unusued terminal, run the following command:

.. code:: bash  

    ros2 topic pub /demo/cmd_demo geometry_msgs/Twist '{linear: {x: 1.0}}' -1



Running turtlebot3
-------------------

Turtlebot3 is an introductory program used to teach people how to work with some of the ROS simulation software.
To start Turtlebot3 in Gazebo, run:

.. code:: bash

    export TURTLEBOT3_MODEL=burger
    ros2 launch turtlebot3_gazebo empty_world.launch.py

While in the simulator, you can create an additional node to allow you to control the robot. Run the following commands **in a second terminal** to add robot control based on arrow key inputs:

.. code:: bash

    ros2 run turtlebot3_teleop teleop_keyboard

Once completed looking around the world, return to the terminal window and press `Control` + `C` to exit. Feel free to run the simulation in any of the available configurations, as defined below:

.. code:: bash

    export TURTLEBOT3_MODEL=[ROBOT]
    ros2 launch turtlebot3_gazebo [WORLD].launch.py

:[ROBOT]:

    The type of robot to run. This can either be `burger`, `waffle`, or `waffle_pi`


:[WORLD]:

    The type of world to load. This can either be `empty_world`, `turtlebot3_world`, or `turtlebot3_house`


As a note, the robots running in the simulation are created from actual robots that can be purchased. While pricy, custom CAD can be imported into Gazebo and controlled with a bit of configuration.

.. image:: images/waffle-robot.png
    :alt: Picture of the consumer ROS waffle robot