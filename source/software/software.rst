.. This document creates a brief overview of this documentation

Software
========

.. toctree::
   
   machine-setup/machine-setup
   development-process/development-process
   development-tools/development-tools
   repository-setup/repository-setup


The software team is responsible for development and maintenance on multiple systems, all managed through our :term: `GitHub` team. The primary systems are outlined below:

**Embedded Robot Code**

:2020-2021:
   https://github.com/msoe-vex/ChangeUp

:2021-2022:
   (Soon to be created)

The embedded robot code controls all of the onboard systems and communication present on our competition robots. This code is primarily written in C/C++ and Python, and is specialized to each robot that our team creates. This code is run both on our :term:`V5 Brain`, as well as our :term:`Compute Co-processor`. Architecture running on our :term:`V5 Brain` are entirely developed in C/C++, whereas the architecture running on our :term:`Compute Co-processor` is Python dominated, with some C/C++ components.

**WebDashboard**

:GitHub:
   https://github.com/msoe-vex/WebDashboard

The WebDashboard is a web interface that allows for the creation of robot paths that can be run on compatible robots. These paths specify waypoints on the field that a robot should travel to within a sequence, with interpolated points to allow the robot to perform clean movements between the points. This application exports the path as a :term:`Robot Path File` in JSON, which is then saved to the robot on an SD card. The application is currently built in JavaScript, with a Typescript refactor in the works.
