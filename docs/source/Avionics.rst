Avionics
========


In an attempt to streamline the installation, and the inevitable replacement of airframes after hard landings, we decided fairly early in our development process to
try and condense the avionics into simple and compact unit, that can be replaced and installed with just two screws into the Mozzie airframe.

The main reasons for pursuing this were:
 * to simplify replacing the complete avionics because of a malfunction
 * to bench-test and repair avionics hardware without the bulk of the airframe impeding access to the various components,
   which in turn allows for a more compact package overall
 * to allow for a quick replacement of the avionics hardware in the competition and testing, and to reduce repair and maintenance time in the field
   (replacement being typically faster than repair)
 * to allow for changes and additions in avionics hardware without affecting airframe layout
 * to reduce rebuild times after a catastrophic airframe failure (crash!)

As a consequence of the integration of the various components into the avionics enclosure, including the pi Camera module and servo tilt mount,
it was possible to use the mass of the enclosure to dampen the camera and FC from airframe and propulsion induced vibration.
It considerably reduced the cabling complexity and cable use in the airframe which is a challenge for a small airframe, and also simplified the camera angle setup because the FC IMU was mounted on, and moved with, the same mechanical structure as the camera.

.. Note::
  The Avionics Enclosure build is divided up into a configuration and assembly sections. It is advisable to complete the configuration setup and bench test the configuration prior to assembling the Avionics Enclosure to avoid having to disassemble the enclosure in order to diagnose a malfunction of misconfiguration.



.. toctree::
   :hidden:

   AvionicsEnclosureAssembly
   PixhawkSetup
   RXSetup
   RFD900xSetup
   PiSetup
   SoftwareSetup
