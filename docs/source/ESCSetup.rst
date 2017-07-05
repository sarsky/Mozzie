ESC Setup
---------

It is important to configure the ESC's for all the motors correctly prior to operating the Mozzie.
The critical settings are motor rotation direction and throttle calibration.

For the quad ESC's we set the internal PWM/PPM Throttle Minimum and Maximum using the BLHeli configuration tool
which in most cases means a ESC throttle calibration for the quad ESCs is not required.

Quad ESC setup
^^^^^^^^^^^^^^^

.. Note::
  These instructions and parameters are specifically for the setup of the ZTW Spider Pro 30A HV ESCs using a Arduino Nano 328 board that can be flashed with the BLHeli bootloader.
  If using different ESCs please check the manufacturers recommended settings for the specific motor and ESC used.

.. image:: /images/BLHeli_ArduinoESC_SM.jpg
    :target: /images/BLHeli_ArduinoESC.jpg

To setup the ZTW ESC download the latest version of `BLHeli Suite <https://blhelisuite.wordpress.com/>`_
Then run BLHeliSuite.exe from the extracted folder you downloaded.

In the "Select ATMEL/ SILABS Interface tab" choose the SiLabs BLHeli Bootloader (USB/COM) hardware option to use the Arduino Nano BLHeli Programmer.

Connect the Arduino Nano to the servo plug of the ESC, making sure the polarity is correct.

Then select the Com port to which the Arduino programmer is connected to and the correct Baud (19600) for the Arduino and click connect. Use the "Read Setup" button to read the current ESC setup parameters,
which should populate the settings values on BLHeli Suite.

Download the `BLHeli_OBC Mozzie FWD  <http://link>`_ and `BLHeli_OBC Mozzie REV <http://link>_` parameter files to a folder on your PC.

Then under the ESC Setup menu item select "Read Setup from ini file" and choose the correct ini file for the motor ESC you are programming.

.. Note::
  Both ini files are identical, the only difference is the motor rotation direction, which can also be changed in BLHeli directly.

Once you are certain the settings are correct use the "Write Setup" button to write the parameters to the ESC.

Finally read the parameters back to confirm they were written correctly and then disconnect the ESC servo wire, and repeat the process for all the quad ESCs.


.. image:: /images/BLHeli_Setup.jpg
    :target: /images/BLHeli_Setup.jpg


Using USB Linker, BLHeli software and configuration file

Forward Motor ESC
^^^^^^^^^^^^^^^^^

Find instructions for fwd ESC.....

Motor brake should really be activated and RC cal done.
