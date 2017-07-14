RFD900x Setup
==============

.. image:: /images/AE/RFD900x/RFD900x.jpg

These instructions should be read in addition to the RFD900x Manual that can be found here: `RFD900x Manual <http://files.rfdesign.com.au/Files/documents/RFD900x%20DataSheet.pdf>`_

PtP software Manual can be found here: `Software Manual PtP <http://files.rfdesign.com.au/Files/documents/RFD900x%20Peer-to-peer%20User%20Manual.pdf>`_

All radio frequency components used for the Mozzie are sensitive to RF interference, from both internal and external sources.
Although the setup described here has been used and tested to the ranges required for the competition this does not guarantee their performance at the event.
We recommend that you investigate and carefully consider ways to improve the performance of you communication links as best as possible, for example by using:

- Higher gain antennas, like an Omni, Yagi or dish
- A mast to get the base radios high above ground
- Dedicated low noise power supplies
- Minimizing ground RF noise and interference by other equipment
- Testing all cabling, including USB/LAN extension cables in a challenge type full system setup


.. Warning::
  These modems are high-power RF devices and it is recommended to power these devices from a separate power supply and not directly from the Flight Controller or USB.

.. Note::
  As described previously in the RC Setup page, there are two ways to connect the RC to the Mozzie for manual control. Please refer to these for more details.


Connecting the RFD900 to the Pixhawk
......................................

The easiest way to connect the RFD900x to the Pixhawk is using a pre-assembled `Pixhawk to RFD900 cable  <http://store.rfdesign.com.au/pixhawk-to-rfd900-telemetry-cable-300mm/>`_ from RFDesign.

.. Tip::
  This cable will typically not include the RFD PPM output from Pin 15 of the RFD900x and this will need to be added if using the RFD900x PPM for RC control.
  Please see the RFD900x Manual link above for more details.


.. image:: /images/AE/RFD900x/RFD900xWiring_SM.jpg
      :target: /images/AE/RFD900x/RFD900xWiring.jpg

|

.. image:: /images/AE/RFD900x/RFD900x_Pins.jpg



Connecting the RFD900 to Computer
......................................

Connect the RFD900x to a PC USB using a compatible USB to FDTI cable that also supplies power to the radio as shown below:

.. image:: /images/AE//RFD900x/RFD900x_FTDI_SM.jpg
      :target: /images/AE/RFD900x/RFD900x_FTDI.jpg

Plug in the USB side of the cable into a compatible USB port that can supply enough power to the RFD900x.

.. Tip::
   It is advisable to use an antenna whenever the RFD900 is powered and to connect the RFD900 to an external power source to avoid power brownouts,
   because not all USB ports can deliver sufficient power to the RFD900.


Radio Configuration using Mission Planner
...........................................

The GCS software Mission Planner includes a tool to configure Sik firmware based radios like the RFD900x.

Please follow the Mission Planner configuration instructions to setup the RFD900 radios <http://ardupilot.org/copter/docs/common-configuring-a-telemetry-radio-using-mission-planner.html#common-configuring-a-telemetry-radio-using-mission-planner>`_

As a guide, the settings we use are as follows:

.. image:: images/AE/RFD900x/RFD900xMPSettings_SM.jpg
       :target: images/AE/RFD900x/RFD900xMPSettings.jpg

.. Warning::
  The air and ground radio setups need to match the types of antenna used and not exceed the EIRP limits of the country you are operating in.
  It is solely the user's responsibility to ensure the settings comply with their country's regulations and with the competition rules.
  More country settings can be found here. <http://ardupilot.org/copter/docs/common-telemetry-radio-regional-regulations.html#common-telemetry-radio-regional-regulations>`_
