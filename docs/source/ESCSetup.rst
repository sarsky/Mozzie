ESC Setup
---------

It is important to configure the ESCs for all the motors correctly prior to operating the Mozzie.
The critical settings are motor rotation direction and throttle calibration.

For the quad ESCs, we set the internal PWM/PPM Throttle Minimum and Maximum using the BLHeli configuration tool,
which, in most cases, means an ESC throttle calibration for the quad ESCs is not required.

Quad ESC setup
^^^^^^^^^^^^^^^

.. Note::
  These instructions and parameters are specifically for the setup of the ZTW Spider Pro 30A HV ESCs, using an Arduino Nano 328 board that can be flashed with the BLHeli bootloader.
  If using different ESCs, please check the manufacturer's recommended settings for the specific motor and ESC used.

.. image:: /images/Propulsion/BLHeli_ArduinoESC.jpg


To set up the ZTW ESC, download the latest version of `BLHeli Suite <https://blhelisuite.wordpress.com/>`_,
then run BLHeliSuite.exe from the extracted folder you downloaded.

In the "Select ATMEL/ SILABS Interface tab", choose the SiLabs BLHeli Bootloader (USB/COM) hardware option to use the Arduino Nano BLHeli Programmer.

Connect the Arduino Nano to the servo plug of the ESC, making sure the polarity is correct.

Then, select the Com port to which the Arduino programmer is connected and the correct Baud (19600) for the Arduino and click "Connect". Use the "Read Setup" button to read the current ESC setup parameters,
which should populate the settings values on BLHeli Suite.


Download the `BLHeli_OBC Mozzie FWD  <https://raw.githubusercontent.com/sarsky/Mozzie/master/3d/BLHeli_OBC%20Mozzie%20FWD%20-%20ZTWSpPro20AHV%20-%20Rev.%2014.3%20-%20Multi_170701.ini>`_
and `BLHeli_OBC Mozzie REV <https://raw.githubusercontent.com/sarsky/Mozzie/master/3d/BLHeli_OBC%20Mozzie%20REV%20-%20ZTWSpPro20AHV%20-%20Rev.%2014.3%20-%20Multi_170701.ini>`_ parameter files to a folder on your PC using a right click and "save link as".

Then, under the ESC Setup menu item, select "Read Setup from ini file" and choose the correct ini file for the motor ESC you are programming.

.. Note::
  Both ini files are identical; the only difference is the motor rotation direction, which can also be changed in BLHeli directly.

Once you are certain the settings are correct use the "Write Setup" button to write the parameters to the ESC.

Finally, read the parameters back to confirm they were written correctly and then disconnect the ESC servo wire, and repeat the process for all the quad ESCs.


.. image:: /images/Propulsion/BLHeli_Setup_SM.jpg
    :target: /images/BLHeli_Setup.jpg
