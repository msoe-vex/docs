.. This document outlines how to install Git on Linux

Installing Git on Linux
=======================

Installing Git on Linux will allow to run any of our repositories, including those with any ROS dependencies that require Linux. This setup will walk you through the install process, and help you set up your Linux environment properly.

Installing the Git Client
-------------------------
Installing the Git Client will allow you to run Git commands from any terminal in your Linux VM. To do this, run the following command:

.. code:: bash

    sudo apt install git -y

This will install the client you need to interact with our repositories.

Configuring the Git Client
--------------------------
In order for us to use Git with our GitHub account we have to link an SSH key between our device and the GitHub account we use. 

Stary by generating a new SSH key. Make sure to use your actual email address in the below command. When prompted, use the default key storage location by pressing ``Enter``. Feel free to enter a password if desired, or  press ``Enter`` twice to proceed with no password (which is much more convenient).

.. code:: bash

    ssh-keygen -t ed25519 -C "your_email@example.com"

Start the ssh-agent in the background

.. code:: bash

    eval "$(ssh-agent -s)"

Add your ssh key to the ssh-agent

.. code:: bash

    ssh-add ~/.ssh/id_ed25519

The next step is to add your public ssh key to your github account. Print out the contents of your public key by running the following command:

.. code:: bash

    cat ~/.ssh/id_ed25519.pub

Copy the output of the command by highlighting the key, and right clicking on it to copy.

..image:: images/copyingPublicKey.png
    :alt: Copying the public key generated in the previous step.

In your browser, go to the |Github new SSH key page|.

Paste the value from the previous step into the key box. Enter an appropriate name and add the key to your account.
    
.. |Github new SSH key page| raw:: html

    <a href="https://github.com/settings/ssh/new" target="_blank">Github new SSH key page</a>


To create commits, git must know what your name and email is. To tell git who we are, run the following commands (obviously replace with your name / email).

.. code:: bash

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"