.. This document outlines the basic commands to run the 2D turtlebot simulator, and start learning about how nodes work

Part 1: Using Nodes
===================

Nodes are essential to the ROS ecosystem. Used as the primary building blocks of the architecture, we can add nodes in to encompass anything we need. Before we get to building them, let's first see how they work.

For the first experiment, open **3 terminal windows**, and space them out on your Linux desktop.

In the first one, run the following command:

.. code:: bash

    ros2 run demo_nodes_cpp talker


This will launch a simple **C++ node** who's job is to publish a message to the network, roughly every second. The message will be print to the terminal each time it is sent, with the amount of seconds since the node was started.

In the second one, run the following command:

.. code:: bash

    ros2 run demo_nodes_cpp listener


This launches a simple **C++ node** who's job is to listen for a "talker node" on the network which is publishing messages. You should see this node start to respond to the previous node we started, printing out all of the messages as they're sent.

Finally, let's test something a little bit more difficult. Run the following command in the third terminal:

.. code:: bash

    ros2 run demo_nodes_py listener


This launches a simple **Python node** which also listens for "talker nodes" on the network. You should see this node start printing out everything that our other listener node is printing. However, this node is in **Python**. In ROS, we're able to seamlessly communicate between nodes in Python and C++ without issue; ROS handles the logistics of sending and recieving messages, and all we need to do is write the code to handle the messages that we're sending and recieving. 

Lastly, let's do one last test. Jump over to the first terminal window you created (with the other two listeners still running), and press `Control` + `C` in the terminal running the talker node. Then, run the following code:

.. code:: bash

    ros2 run demo_nodes_py talker

A new **Python** node will be created, publishing messages to the network. Similar to before, you should see both of the listener nodes start printing out messages again. As mentioned before, ROS allows for seamless communication between languages, with only a small amount of overhead.