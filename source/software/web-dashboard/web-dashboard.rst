Web Dashboard
=============

The Web Dashboard is a web interface that allows for the creation of robot paths that can be run on compatible robots. These paths specify waypoints on the field that a robot should travel to within a sequence, with interpolated points to allow the robot to perform clean movements between the points. This application exports the path as a :term:`Robot Path File` in JSON, which is then saved to the robot on an SD card. The application is currently built in JavaScript, with a React rewrite in progress.

:GitHub:
   https://github.com/msoe-vex/web-dashboard

:Live Website:
   https://dashboard.msoevex.com

.. toctree::

   web-dashboard-setup
   web-dashboard-architecture
   web-dashboard-technologies