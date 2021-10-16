.. This document goes over the git submodule command, how it works, and how it can be used

git submodule
=============

The ``git submodule`` command isn't used often within our repositories. Specifically, only our **ChangeUp** repository currently uses :term:`Submodules`. This command allows you to manage your :term:`Submodules` within a repository, pulling updates from each and making sure they are initialized correctly.

Submodules are links from one repository to another within Git, allowing developers to pull in code from other projects *without needing to hand copy-and-paste files between projects*. 

In order to pull in these projects, we can either tell Git that we need the remote code when we *clone* our project, or after we've cloned it. The ``git submodule`` command is specifically used to pull in and manage these remote submodule repositories after we've cloned the remote code.

For example, if you've just recently cloned in the *ChangeUp* repository and need to pull in code for the submodules, you would run the following:

.. code:: bash

    git submodule init 
    git submodule update

These two commands are used **in this order** to first create the links to the remote repositories, and then pull in the most updated code from each.

Command Usage
-------------

.. code:: bash

    git submodule [ARGUMENT]

**Optional Arguments:**

:init:
    Initialize the submodules in your current repository. This will go out to each of the linked repositories, and create a connection to allow the code from each to be pulled into your repository. This command **does not** pull in any code - only initializes the connections.

:update:
    Update each of the links to the submodules. This command will go to each link, pulling in the code from each repository into the respective folder(s) that the submodule links are connected to within your repository. For instance, if you link a folder called ``eigen`` to the remote Eigen repository, this command will pull in all of the code from that remote repository into the linked ``eigen`` folder.