Install Docker
==============

For our development environment, we use Docker.

These install instructions have been borrowed from the `Docker Install Instructions Page`_.


First, update your package lists

.. code:: bash

    sudo apt-get update

Then, install the Docker dependency packages

.. code:: bash

    sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

Add Docker's official GPG key 

.. code:: bash

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

Add the Docker repository to your repo lists

.. code:: bash

    echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


Install Docker Engine from the apt package index

.. code:: bash

    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io

Since we don't want to have to type ``sudo`` every time we run a Docker command, we will add ourselves to the Docker user group

.. code:: bash

    sudo usermod -aG docker $USER

At this point, you will need to log out of your Ubuntu session and log back in. This will cause linux to recheck which user groups you are in and change your permissions accordingly. Log out by clicking near the power icon in the top right corner, then click ``Log Out`` and ``Log Out`` again. Log back in and open up the terminal.

To check that we sucessfully installed Docker, run the following command 

.. code:: bash

    docker run hello-world

If Docker has been installed correctly, you should be greeted by a Hello message. Congratulations!

.. _Docker Install Instructions Page: https://docs.docker.com/engine/install/ubuntu/