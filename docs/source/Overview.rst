Overview
=================

The original idea for the Mozzie project was to create a UAV Challenge READY Quadplane based on the Mini Talon, using both commonly available and some custom 3D printed parts, all for under $1000USD.

This is a complete build instruction wiki to assemble a "Mozzie" quadplane identical to what was used by PerthUAV in the 2016 Medical Express UAV Challenge.

Our intention is that the Mozzie can be used as a base platform to develop systems and technology for UAV challenges, or even as the actual platform being used in a UAV challenge.
This is also our attempt to give back to the Ardupilot and other UAV open source communities, for all their efforts and work, that has made the Mozzie platform possible in the first place.

Through the years that we have been involved in the UAV Challenge we found that many of teams that attempted the challenge were often challenged by only having a limited amount of time,
funds and experience with existing systems, despite having good ideas in overcoming the challenge hurdles themselves. Operating large, complex and expensive airframe systems can often result in
teams running out of time, funds and team resources before they can even participate in the event.

The Mozzie platform and documentation tries to overcome these hurdles by offering a single resource for the completion of a mission capable system that can be competitive in the event.
In turn we hope this results in a popular uptake of the Mozzie platform, so that users can contribute back with design and implementation improvements over time, to make the platform even better.


.. image:: images/Hopper.jpg
    :scale: 100%

.. Note::
   This wiki page is a work in progress and will be completed as the
   information becomes available and the project develops.

The UAV Medical Express Challenge
----------------------------------

The 2018 Medical Express UAV Challenge is a UAV Challenge that is held bi-annually in Queensland Australia.
Broadly the intention of the Challenge is to promote civilian use of UAV technology for humanitarian use, and develop systems for saving lives using UAV technology.
The 2018 Challenge is to fly a "robotic" autopilot controlled aircraft up to 30km away to a remote landing site where it must accurately find and land on a ground target near "Outback Joe",
to collect a 25g blood sample vial and return it intact to base.

The main "challenges" to complete the mission objectives are:
 * Overcome the range required with an aircraft of up to a total of 60km, including landing on the remote site and return inside of 60 minutes
 * Be able to land at the remote site that is cluttered and does not allow for low glide slope landings (10m radius) and
   so should be able to land and takeoff vertically at the remote site to receive maximum points for accuracy on target
 * Must maintain a continuous communications link between the aircraft and base (even whilst on the ground at the remote site)
 * Must stay within a preset geofence at all times
 * Must be able to do this without a human operator influencing the mission control (For the Autonomy Challenge)
 * Must be able to avoid Dynamic No Fly Zones as well as Geofence and No Fly Zones (To achieve the DNFZ Avoidance Challenge)

The current form of the Mozzie is our 2016 attempt to address the UAV challenge and as such does not facilitate solutions for all the latest rule change requirements.
We expect to add solutions as they come to hand from users who participate in the further development of the platform, however,
we offer no guarantee as to the performance of the Mozzie at the event, as this is ultimately the responsibility of the Challenge participants themselves.
We sincerely hope that the information provided here will assist teams in developing their own systems and improvements to the Mozzie platform, that increases their chance of winning the challenge.

More Information on the 2018 Medical Express UAV Challenge can be found here:
https://uavchallenge.org/medical-express/

Introduction to Quadplanes
---------------------------
The Mozzie was specifically developed as a quadplane and to achieve the challenge range, VTOL and speed requirements.
It does this by leveraging two completely separate propulsion, lift and control systems.

One of those systems is represented by the typical aircraft layout by using wings for lift, with control surfaces for manipulating aircraft attitude,
and the forward electric motor for producing thrust. The other flight system is essentially a quadcopter, which produces vertical lift by producing downwards thrust using electric motors,
and by varying motor revolutions it can modulate aircraft attitude control. It's noteworthy that either system can operate independently in the Mozzie, and they are only linked by using the same battery and flight controller,
so either flight system is capable of keeping the Mozzie airborne should the other flight system fail in flight.

Either flight system can also be leveraged to assist the other in flight by allowing each flight system simultaneous control in certain flight situations.
For example wing stall can be eliminated by using the quad assist feature to produce thrust when the forward airspeed does not suffice to produce enough lift with the wings.
This also assists in control authority in low airspeeds where the quad assist thrust can allow maneuverability beyond what the aircraft can manage with wings alone.
This in turn means a more aggressive AoA of the wings can be used in flight which reduces quad motor load in conjunction with forward motor assist,
particularly in strong wind situations this can improve hover efficiency significantly because the Mozzie wings continue to produce lift.

Having two flight systems also affords the Mozzie a redundant flight recovery system should one system fail. The Mozzie can takeoff and land in both forward and quad mode. (forward takeoff recommended with bungee)

Another benefit of adopting two separate flight systems is the ability to optimise each of those flight systems for the intended flight profile.
For the challenge the aircraft system will predominately be operated in forward flight mode utilizing the wings for lift, as this is the most efficient way to achieve the cruise speed and range required for the mission.
The quad flight system only serves a short term secondary role, in that it allows the Mozzie to land and takeoff at the remote site,
whilst it can land and takeoff in forward flight at base should the battery not suffice for a softer quad type landing.

To optimize each of these propulsion systems it is important to prioritize forward winged cruise over hover efficiency, because the Mozzie will typically only hover for one or two minutes in the challenge mission overall.
By using a bungee or quad takeoff it is also possible to optimise the forward propulsion so that with the forward motor both pitch speed and thrust equals drag at cruise velocities,
without the need to ensure enough static thrust is provided by the forward motor for takeoff. The quad motors and props can also be optimised for forward flight,
in that they are as small as possible, creating the least possible drag and weight for forward flight whilst being sufficient to lift and control the Mozzie in hover.
The overall gain in forward cruise efficiency, by optimising the drivetrain for forward flight over a longer period, more than compensates for the losses created by using a high disc loading quad lift system.

All of these optimisations only add value if the other systems used in the Mozzie can also achieve their mission objectives as well.
The camera system is particularly important for locating the ground target, and as such it's important to ensure that the camera system can operate in the prevailing flight conditions, and in fairly turbulent or fast forward flight.
Limiting the design to only have a short hover time also means that it's not possible to use extensive hover times to image the search area and find the target.
In our experience, however, forward winged flight resulted in better and more stable imaging than in hover, so having limited hover times had negligible impact on mission outcomes.

Overall we are very happy with the potential and the performance of the Mozzie QP platform, and we look forward to seeing more projects based on this platform!



Specifications
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
Cruise Current   4-6A       On 4S 10Ah Battery
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
