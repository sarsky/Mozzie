Pixhawk
=======

The Mozzie platform is currently pre-configured to run on the Ardupilot Pixhawk platform and is heavily reliant on the Arduplane quadplane development.
To avoid overlap and the need for updating the Mozzie build documentation pages on each Arduplane release,
we have predominately linked to the Arduplane pages for configuring the Pixhawk and have only added our Mozzie specific customizations here.

Any VTOL capable autopilot that can be configured for a quadplane should be able to operate the platform as well and we welcome any such additions.


.. Note::
  For ease of configuration we have a pre-configured parameter file for the Pixhawk that should get the airframe airborne with some basic tuning.
  The Mozzie parameter file is dependent on a similar propulsion setup and airframe layout, and should always be tuned for each aircraft separately.

.. Tip::
  If a custom propulsion setup is used we recommend that the quad components have a lift to weight ratio of over 1.7 (so 2.5kg MTOW should have around 4.2kg lift).


Ground Control Software GCS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For ease of use and compatibility with the latest Arduplane development we recommend using the Mission Planner GCS that can be downloaded here:

`Latest Mission Planner Download <http://firmware.ardupilot.org/Tools/MissionPlanner/MissionPlanner-latest.msi>`_

Mission Planner installation instructions for Windows can be found here:

`MP Installation <http://ardupilot.org/plane/docs/common-install-mission-planner.html>`_

Mission Planner can install the firmware, modify and upload the parameter files and be used for Mission Control.
A full list of instructions and features can be found here:

`Mission Planner Docs <http://ardupilot.org/planner/index.html>`_


Pixhawk Firmware
^^^^^^^^^^^^^^^^^

We will endeavor to release a parameter configuration file for each new Arduplane release.

Please follow these `Instructions <http://ardupilot.org/plane/docs/common-loading-firmware-onto-pixhawk.html>`_ to install the autopilot firmware and select Arduplane 3.7.1 firmware version to install.

The Arduplane 3.7.1 Mozzie parameter configuration file can be downloaded here: `Mozzie.param <http://link>`_

Once the firmware is successfully installed, and whilst the Pixhawk is still connected via USB, go to the Mission Planner Config/Tuning tab
and select the "Full Parameter List" Menu item on the left of the screen. Then use the green "Load from File" button on the right and select the
Mozzie.param that was downloaded above and use the Green "Write Params" to write the Mozzie parameters to the Pixhawk.

.. Tip::
  Writing the Mozzie parameter file should overwrite all the parameter data on the Pixhawk. Please confirm this by using the Mission Planner compare feature.


Pixhawk Wiring
^^^^^^^^^^^^^^

As described in the Avionics Assembly section the Pixhawk wiring should be connected as per the following schematic:

.. image:: .... image:: images/PXH_Wiring_SM.jpg
        :target: images/PXH_wiring.jpg

.. Tip::
  Further more detailed wiring information specifically for the Pixhawk can be found on the Ardupilot documentation pages here: `Pixhawk Wiring <http://ardupilot.org/plane/docs/common-pixhawk-wiring-and-quick-start.html>`_


.. Note::
  Further information for configuring the Mozzie before flight can be found in the "Flying the Mozzie" section, which includes RC calibration and PXH configuration checks.
