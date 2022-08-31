Using Git
=========

``git`` is a Command Line Interface (CLI) for working with GitHub. It provides a convenient interface for working with GitHub.

Terminology
-----------
.. glossary::
    Repository
        A GitHub container which contains the entire project.
    Origin 
        A GitHub term used to refer to things stored by GitHub on the cloud. In most cases, things on the cloud cannot be edited directly.
    Local
        A GitHub term used to refer to things stored on your local machine.
    Branch
        A Branch is simply a code workspace containing some version of the code defining a repository.
    Master
        By convention, ``master`` is the name of the branch in a given Repository containing the code that is actively being used in production. In the real world, ``master`` is often carefully protected to prevent interns from accidentally breaking the internet; hence, changing ``master`` directly is usually not allowed. However, ``master`` can still be freely copied onto a local machine or copied to another branch.
    Pull Request
        A pull request is a request for two Branches to be merged together. 

Standard Workflow
-----------------
The standard workflow for making a change to a project is as follows:
    1. Create a local copy of the branch you'd like to make changes to.
    2. Push the local copy of the branch to the cloud so it also exists in GitHub.
    2. Make changes to the local copy of the branch and push them to the branch on the cloud.
    4. Once your branch is finished, create a pull request asking to merge your new version of the branch into the original branch.

Step by Step Guide
------------------
With that out of the way, the complete workflow for making changes to a branch is as follows.
    1. If you haven't already, clone the repository onto your machine.
    2. Open the branch you'd like to change on your local machine. 
        * You can view all branches using the command ``git branch -a``.
        * You can switch branches using the command ``git switch branch-name``.
    3. Create a local copy of the branch.
        * This can be done using the command ``git checkout -b new-branch-name old-branch-name``
    4. Open the local copy of the branch using the command ``git switch new-branch-name``.
    5. Make changes. As you make changes, you should periodically add your changes using ``git add <file_path>`` and commit them
        using ``git commit -m "<commit_message>"``.
    6. Push your changes to the cloud using ``git push``.
    7. On GitHub, make a pull request requesting to merge your changed branch with the original branch you wanted to edit.