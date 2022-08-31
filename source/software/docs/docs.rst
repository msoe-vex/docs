Docs
====

Linux
-----
First, install Python 3 and the pip Python package managers.

.. code:: bash

    sudo apt install python3 python3-pip python3-venv


If you haven't already, clone the docs repository

.. code:: bash

    git clone git@github.com:msoe-vex/docs.git

Move into the docs repository directory and create a Python virtual environment. It is always a good idea to create separate Python virtual environments for each project you work on. Python virtual environments can save you a lot of headache with package incompatibilities in the long run.

.. code:: bash

    cd docs
    python3 -m venv venv

Next, we source our newly created virtual environment

.. warning::

    It is important that you remember to source the virtual environment each time you open a terminal session and want to interact with the docs repo. 
    If you forget, you will get errors about packages not being available.

.. code:: bash

    source venv/bin/activate


Your bash prompt should now be prefixed with ``(venv)`` to show that you are in the Python virtual environment.

We now need to install the required Python packages to build the docs repo. We do this by telling pip to install all the packages in the requirements.txt file in the root of the repo.

.. code:: bash

    pip install -r requirements.txt 


Try building the docs repo by running the following command

.. code:: bash

    make html

If the installation was successful, the sphinx docs html pages should now build successfully. You can view the locally built docs by running:

.. code:: bash

    firefox build/html/index.html &

Windows
-------

First, install python3 (from the windows store):
`python3<https://www.microsoft.com/store/productId/9PJPW5LDXLZ5>`_

Next, clone the docs repo and move into it:


Next, install sphinx using the command line:

.. code:: shell

    pip install -U sphinx

By default, sphinx won't be on PATH. To update it, run the command:
.. code:: shell
    
    some code

You can then activate the virtual environment using the command:
.. code:: shell

    .\venv\Scripts\activate.bat

Then run the following command to install the required packages.
.. code:: shell

    pip install -r .\requirements.txt

Lastly, run 
