===================================================================================
Building the Mozzie
===================================================================================

A UAV Challenge READY Quadplane based on the Mini Talon for under $1000USD.

This is a complete build instruction to assemble a "Mozzie" quadplane identical to what was used by PerthUAV in the 2016 Medical Express UAV Challenge.

.. image:: images/Hopper.jpg
    :scale: 100%

.. tip::

   This wiki page is a work in progress and will be completed as the
   information becomes available and the project develops.

Overview
=========

The complete instructions and files required to build a Quadplane capable of attempting the UAV Medical Express Challenge.....
ADD Some challenge details....

Specification
==============

=============== ========== =======================================================
**Hardware**    **Value**  **Note**
=============== ========== =======================================================
MTOW            2.5kg      Maximum Take-Off Weight
Payload           1kg      Max Payload (incl. Battery)
Wingspan        1300mm
Length          830mm
Wing Area       30dm^2
Wing Load       80g/dm^2
Battery         4S 10Ah    Recommended battery
=============== ========== =======================================================

================ ========== =======================================================
**Performance**  **Value**  **Note**
================ ========== =======================================================
Cruise Current   4-5A       On 4S 10Ah Battery
Vno              22-29m/s   Nominal Cruise Speed (Forward)
Vne              35m/s      Never Exceed Speed (Forward)
Vs               16m/s      Stall Speed (Forward/Wings Only!)
Max Endurance    90min      In Forward Flight
Max Range        90km       In Forward Flight
Wind Penetration 14m/s      In hover + forward
Max Hover Time   12min      Hover only
VTOL & Forward   75min      2x VTOL and 72min Forward Flight
================ ========== =======================================================

================ =========== =======================================================
**Avionics**     **Item**    **Note**
================ =========== =======================================================
Autopilot        Pixhawk     Ardupilot 3.7.1 (with Quadplane Control)
Telemetry        RFD900x     With Mesh Relay and PPM (40km range)
GPS              M8N         (Optional RTK)
Airspeed         Digital     Quad Assist Stall Prevention
Comp. Computer   Pi Zero W   Running Mavproxy, imaging, 3G modem and wifi
Camera           PiCam 8MP   With geotagging Mavproxy module and servo tilt
Redundant Power  3x          With separate Failsafe power
Flight Modes                 Auto, RTL, Windvaning Loiter
================ =========== =======================================================

|
|
