Install Visual Studio Code
==========================

.. warning:: 

    Be sure to pay attention to if commands/actions should be taken on Windows/Linux when following this page
    

Downloading Visual Studio Code
------------------------------

On **Windows**, download and install Visual Studio Code from the `Visual Studio Code download page`_.

Open up Visual Studio Code. We need to install the Remote Development extension pack, which we can do by opening up the extensions tab (keyboard shortcut Ctrl+Shift+X).

Setting up SSH Keys
-------------------

Run the following commands in powershell to generate a ssh rsa key and copy it onto your Linux virtual machine. Make sure to replace username with your Ubuntu account username.

.. code:: powershell

    ssh-keygen -t rsa -b 4096 -f "$HOME\.ssh\linux_rsa"
    scp -P 3022 "$HOME/.ssh/linux_rsa.pub" username@127.0.0.1:~/key.pub

On **Linux**, install ssh server

.. code:: bash

    sudo apt install openssh-server

Add the ssh key generated in Windows to the list of authorized keys. This will allow us to connect to our linux virtual machine over ssh without having to type our password every time.

.. code:: bash

    cat ~/key.pub >> ~/.ssh/authorized_keys
    rm ~/key.pub

Visual Studio Code Setup
------------------------

Opening Visual Studio Code on **Windows**, we should see a green icon in the lower left hand corner of the screen. Click on that icon and select ``Open SSH Configuration File..``. If prompted, select the path that looks like ``C:\Users\username\.ssh\config`` and in the file that opens, paste in the following replacing ``username`` with your linux username.

.. code::

    Host lvm
        HostName 127.0.0.1
        Port 3022
        User username
        IdentityFile ~/.ssh/linux_rsa

Click on the green icon again, but this time select ``Connect to Host``, then select ``lvm``. If prompted for the remote machine type, select ``Linux``. 

If everything was set up correctly, you should *not* have to enter your Linux password and should be presented with an empty project screen with a linux command prompt in the terminal view.


.. _Visual Studio Code Download page: https://code.visualstudio.com/download