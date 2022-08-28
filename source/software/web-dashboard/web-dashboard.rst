Web Dashboard
=============

The Web Dashboard is a web interface that allows for the creation of robot paths that can be run on compatible robots. These paths specify waypoints on the field that a robot should travel to within a sequence, with interpolated points to allow the robot to perform clean movements between the points. This application exports the path as a :term:`Robot Path File` in JSON, which is then saved to the robot on an SD card. The application is currently built in JavaScript, with a React rewrite in progress.

:GitHub:
   https://github.com/msoe-vex/web-dashboard

:Live Website:
   https://msoe-vex.github.io/web-dashboard/www/

Setup
-----
The Web Dashboard uses Node.js (aka npm) to manage packages and dependencies.
If you don't have Node.js installed, you can download it here: `Node.js <https://nodejs.org/en/download/>`_

After installing Node.js, you should clone the web-dashboard repository from msoe-vex/web-dashboard.
   1. Open VS Code, then choose ``Source Control`` in the left toolbar. 
   2. Click the three dots in the top right of the panel that opens and choose ``Clone``. 
   3. In the toolbar at the top, click ``Clone from GitHub``, then enter ``msoe-vex/web-dashboard``.
   4. Specify a location where the web-dashboard repository clone should go.
   .. tip::
      It's reccomended to create a single folder named ``raider-robotics`` to contain all of your robotics related code.
   5. Click confirm. A copy of the web-dashboard repository will be placed a new folder named ``web-dashboard`` in your specified location.

By default, web-dashboard will contain the files on the default branch of the ``web-dashboard`` repository. The default branch is currently the react rewrite branch ``react-rewrite``.
To launch a copy of the website on your local machine:
   1. Open a terminal in VS Code using ``Ctrl+Shift+```.
   2. Run the command ``npm install`` to automatically install all dependencies.
   3. Run the command ``npm start`` to launch the ``web-dashboard``.

.. To learn more about editing branches using git, see