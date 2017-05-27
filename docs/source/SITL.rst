Simulation with SITL
=======================

SITL allows you to plan flight missions and simulate test aircraft parameters without risking
your actual aircraft. To set it up you will need a SSH client like: 
* link mRemoteNG: https://mremoteng.org/download
* link Putty: http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

Step 1 - Setup SSH Client
...........................

First add a new connection to the SSH client using these settings:


================ ==================
Item             Setting
================ ==================
Connection Name  PUAV SITL
Hostname or IP   81.169.245.85
Port             22
User             puav
Password         Nandos842
Protocol         SSH v2
================ ==================


Step 2 - Start SITL
...................

Connect to the server using the settings above.

At the Command prompt type or copy paste this text to change to the right directory::

    cd ardupilot/ArduPlane

.. Tip::
  To copy paste into a SSH session use Ctrl-C to copy the text and use the right mouse button to insert into the SSH session on the command line.

Then enter one of the commands below to start SITL using the desired options for aircraft and location:

WA Melros Beach (School oval)::

    sim_vehicle.py -j4 -L WAMB -f quadplane

WA Aubin Grove::

    sim_vehicle.py -j4 -L WAAG -f quadplane

WA Salt Lakes::

    sim_vehicle.py -j4 -L WASL -f quadplane

WA Sutherlands Park::

    sim_vehicle.py -j4 -L WASP -f quadplane

Or the MEC Challenge in Dalby QLD::

    sim_vehicle.py -j4 -L Dalby -f quadplane

Once the command has run it should return with the current flight mode. For example: FBW>

.. Tip::
  You can add a custom location to the ardupilot/Tools/autotest/locations.txt by running::

    sudo nano ardupilot/Tools/autotest/locations.txt

  In that text file you can add locations using the following format:
  To change locations add Lat, Long, Alt, Heading like: WAMB=-32.625106,115.632251,10,0

Step 3 - Connect GCS
......................

Then connect to SITL by adding an output after SITL has started using you actual IP address where your GCS is connected::

    output add "your ip"":14551

For example it should like "output add 123.456.789.123:14551" but with your own IP address

Step 4 - Load Mission and Geofence
...................................

Open your GCS and connect to SITL using UDP.
It will then ask for the port so use: 14551.

.. Tip::
  Make sure the port is allowed through your router to the computer running your GCS.

Then create and upload a mission to the Flight Controller as described here:

If required create and upload a Geofence to the Flight Controller as described here:

.. Note::
  You can use the GCS to control the aircraft and mission from now on as if it were a real aircraft.
  The following is only required if you want to run it using Mavproxy commands instead or you want to change the simulation settings like wind and direction.

.. Tip::
  For flights with a real aircraft a geofence is a good way to protect property and persons, as well as making sure you can recover the aircraft if something goes wrong.
  Trying out the geofence in SITL will give you the confidence to use it in real missions.

Alternatively you can load one of the preset missions for the same location you chose previously using the following command and the relevant mission \*.txt file. Make sure there is a txt file mission available with that name.

For Example::

    wp load ../Tools/autotest/ArduPlane-Missions/TEST.txt

.. Tip::
  It's good practice to make sure the mission is successful using SITL before flying it with a real aircraft.

Run and Change Simulation using Mavproxy (Optional)
...............................................................

Like on the real aircraft the Throttle Safety Switch must be armed before the motor will engage for flight::

   arm throttle

To start flying the mission you have uploaded to your GCS (or preset mission you have loaded) use::

    mode auto

Common Mavproxy commands you can use in flight via the command line:



Changing Simulation
....................

Whilst flying it is possible to change the wind direction and speed to simulate weather
affects on the aircraft using these two commands and changing the numbers at the end (wind speed is in m/s and direction is in degrees from North)::

   param set SIM_WIND_SPD 4
   param set SIM_WIND_DIR 220

.. Tip::
  If there is an issue with the parameter file use this to set it to default::
    sim_vehicle.sh -w
