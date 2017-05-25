Avionics Enclosure Assembly
===============================


3D Parts Required:
 - Avionics Enclosure Pi (bottom)
 - Avionics Enclosure RFD/Air (top)
 - Avionics Enclosure Plate (center)
 - Avionics Enclosure Front Mount

 - Avionics Enclosure Rear Mount
 - Avionics Enclosure Screw Washers
 - Pi Camera Servo Mount
 - Pi Camera Holder

 .. Tip::
     Not all 3D parts come off the printer in perfect condition. Before assembling or gluing any 3D printed parts ensure that the parts all fit together by carefully removing any excess plastic from the print and seeing if they dry fit together first!


Components Required
 - Airspeed Sensor
 - I2C Bus
 - FrSKy XSR RC Receiver
 - RFD900x Radio Modem
 - GPS M8N
 - Pi Zero W
 - Pi Camera Module v2
 - Pi USB Hub Zero4U
 - Pi Reboot Relay
 - 1x Servo DS-929
 - Pixhawk

Step 1 -  Pre-Assembling the Avionics Enclosure
................................................

As always it's a good idea to make sure the 3D printed part fit first without any components installed.

.. image:: /images/AE/3DPrintAs.png
    :scale: 100%

Assemble the Avionics Enclosure (AE for short) Pi, RFD/Air and Center plate as follows, taking care to align the plastic and making the parts fit together seamlessly.

.. todo::
   image:: /images/AE/MountBallsCenter.jpg
   
   Make image!

Insert the rubber isolation balls into the Avionics Center Plate as shown.

.. tip::
  To mount the rubber balls into the mounts and enclosure center plate insert them on one side first then carefully pull the rubber ring through the hole until the rubber is flush all the way around the hole.



Step 2 - Assembling the Pi Avionics Enclosure
.................................................

Connect the Pi camera ribbon cable to the Pi Camera with the contacts of the ribbon cable facing the picamera PCB.

.. image:: /images/AE/ServoMountCam.jpg
    :scale: 100%

Then ensure the slot on the Pi Camera Servo Mount is clear and insert the Pi Camera ribbon cable in the orientation as shown.
(note this must be the correct way otherwise it will not connect to the Pi Zero connector properly)

.. image:: /images/AE/ServoMountAs.jpg
    :scale: 100%

2x images one for plug one for assembled 979 981

Insert the Servo plug into the Camera Servo Mount as shown, making sure there are no twists in the cable so the Servo fits seamlessly into the mount.
Screw the servo to the mount using the screws provided with the servo.


.. image:: /images/AE/ServoToPiAE.jpg
    :scale: 100%

3x images 1) insert cables 987 2) Side Screw 988 3) route cables 993

Insert the cables through the Pi AE as shown, attach the Camera Servo Mount to the Pi Avionics Enclosure using the XXmm screws, and route the cables internally as shown above.
Note the servo cable should be flat and routed inside the Pi mount "screw studs??" and then out the rear of the enclosure

.. image:: /images/AE/PiNHub.jpg
    :scale: 100%

image 994

.. Tip::
  Use a XXmm metal screw to thread the 3D printed extrusions prior to using plastic screws to attach the Pi to the enclosure.

Take the completed Pi and USB assembly constructed in Wiring and Configuration Setup phase, place it into the Pi AE and attach it with the USB HUB supplied plastic screws.
Route the cables as shown.

.. image:: /images/AE/PiAEToCenter.jpg


2x image 1) route cables 1000  2) centerplate attached 1001

Route the two DF13 Cables as shown through the Center Plate and place Center plate on Pi AE.

Step 3 - Assembling the Air/RFD Avionics Enclosure
....................................................

.. todo::
   image:: /images/AE/AirAEComp.jpg

   4x Image 1) I2C 964 2) + Airspeed 965 3) + XSR 1009 4) +GPS 1010

Insert I2C Hub into Air AE, then the Airspeed Sensor and XSR RC receiver (if used) with the binding button facing upwards as shown. Attach and route the two I2C cables, one between the Airspeed and I2C bus and one I2C cable to the outside of the enclosure via the opening under the XSR receiver.
Route the XSR servo connector out through the opening under the XSR.

.. todo::
   image:: /images/AE/AirAECompGPS.jpg
  
   Image 1011

Next insert the connectors of the GPS module on an angle through the top right opening of the Air AE.
The 4pin  Connector plugs into the I2C hub and the 6 pin connector is routed out through the opening underneath the XSR.

.. todo::
   image:: /images/AE/AirAECompRFD.jpg
  
   Image 1012

The RFD900 module cable can the be routed through the Airspeed sensor side opening, and can be placed with the antenna plugs through the enclosure and clipped into place.
(The extra space in the Air/RFD AE can also be used to connect a secondary 3DR modem if required. For example for 433MHz)

.. Note::
  Make sure that various cables are routed correctly, and are not taut, or caught between components.




Step 4 - Final Assembly of the Enclosure
....................................................

.. todo::
   image:: /images/AE/PiAEToAirAECable.jpg
  
   Make new picture!!

Place the two DF13 cables through the opening of the Air AE next to the Airspeed Sensor back outside of the enclosure.

.. todo::
   image:: /images/AE/PiAEToAirAE.jpg
  
   image 1014

Carefully place the Air AE over the Center Plate making sure that the cables are clear of the contact areas and are long enough to reach their respective PXH connectors.
You can use two screws to hold the enclosure together while you organize the PXH connectors.

.. Note::
  Some cables might be longer than necessary so if required the extra length can be contained in the enclosure to make the cable management neater.

It should look something like this:

.. todo::
   image:: /images/AE/AEAs.jpg
  
   make new image


Step 5 - Attaching and Connecting the Pixhawk
....................................................

.. todo::
   image:: /images/AE/AEPixhawk.jpg
   
   image 1016

The Pixhawk can now be mounted using double sided foam tape, on the top of the Avionics Enclosure with Servo pins on the same side as the RFD antennas.

.. Tip::
  Try to align the PXH straight onto the enclosure before sticking it in place

.. todo::
   image:: /images/AE/AEPixhawkCables.jpg
 
   image 1021

The cables can now be connected to the Pixhawk as follows:

On the left side of the Pixhawk:
 1) RFD cable to Telem 1
 2) Pi Serial to Telem 2
 3) Power from Pi to USB (This is the third redundant power supply)
On the right side of the Pixhawk:
 1) GPS cable to GPS
 2) I2C bus cable to I2C
And in the middle:
 1) The Switch to the Switch and the
 2) The speaker/Buzzer to the Buzzer

.. todo::
   image:: /images/AE/AEPixhawkCables2.jpg
    
And then finally insert:
 1) the XSR Servo connector into RC IN
 2) the Camera Servo Connector into RC 11 (Aux 3)
 3) the Pi Reset Relay Servo connector into RC 12 (AUX 4)

The last thing to do is route the XSR Antenna's through the top opening and through the Antenna holder tubes. (Heat shrink the antenna cables once attached to the enclosure to strengthen the frail cables against damage)

 .. Note::
   The Front Servo connector should never be inserted into the Pixhawk or any standard servo connector as it is not compatible and can only be used with the LED strip as specified.
