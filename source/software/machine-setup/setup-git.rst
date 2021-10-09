Git Setup
=========

Generate and Add an SSH Key to Github
-------------------------------------

Generate a new SSH key. Make sure to use your actual email address in the below command. When prompted, use the default key storage location by pressing ``Enter``. Feel free to enter a password if desired, or  press ``Enter`` twice to proceed with no password (which is much more convenient).

.. code:: bash

    ssh-keygen -t ed25519 -C "your_email@example.com"

Start the ssh-agent in the background

.. code:: bash

    eval "$(ssh-agent -s)"

Add your ssh key to the ssh-agent

.. code:: bash

    ssh-add ~/.ssh/id_ed25519

The next step is to add your public ssh key to your github account. Read your public key by running the following command

.. code:: bash

    more ~/.ssh/id_ed25519.pub

In your browser, go to the |Github new SSH key page|

Copy the output of the above command (highlight and right click to copy) and paste it in the key box. Enter an appropriate name and add the key to your account.
    
.. |Github new SSH key page| raw:: html

    <a href="https://github.com/settings/ssh/new" target="_blank">Github new SSH key page</a>

Configure Git Email and Name
----------------------------

To create commits, git must know what your name and email is. To tell git who we are, run the following commands (obviously replace with your name / email).

.. code:: bash

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
