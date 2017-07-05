RX Setup
==============

Optional FrSky PPM setup to RFD900x for RX connection or FrSky RX in Mozzie
Binding with RC and Link to instruction.

.. note::
  There are two ways to use a FrSky receiver in the Mozzie:
  1. By connecting it directly to the PPM input of the Pixhawk (instead of the RFD900x PPM output)
  2. By connecting it as a PPM input to the RFD900x IO pin 15 (this also means you are only relying on the RFD900x for RC control of the UAV, but you will have RFD900x RC range well beyond line of sight)


Specifications
...................

| Dimension:26x19.2x5mm (L x W x H)
| Weight: 3.8g
| Number of Channels: XSR- 16Ch ( 1-16ch from SBUS channel, 1-6ch from CPPM Channel)
| Operating Voltage Range: 4.0-1OV
| Operating Current: 1OOmA@5V
| Firmware Upgradeable
| Compatibility: FrSky X-series Module & X9D & X9DP & X9E & X12S in D16 mode
| (XSR does  not work with D-series Module)
|

**Features:**

  •	Smart Port enabled, realizing two-way full duplex transmission.
  •	S-BUS output
  •	CPPM output


Binding Procedure
...................

Binding is the process of uniquely associating a particular receiver to a transmitter module. A RC transmitter can be bound to multiple receivers (but can't be used simultaneously). A receiver can only be bound to one transmitter module at a time.

The binding procedure is as follows.

  1.  Turn on the transmitter while holding the F/S button on the module or by selecting bind in the on screen menu (please refer to the module instruction manual for switch positions). Release the button. The RED LED on the Module will flash, or the Transmitter will beep, indicating the transmitter s ready to bind to the receiver.
  2.  Connect battery to the XSR receiver while holding the F/5 button on the receiver. The LED on the receiver will flash, indicating the binding process is completed.
  3.  Turn off both the transmitter and the receiver.
  4.  Turn on the transmitter and connect the battery. The GREEN LED on the receiver indicates the receiver is receiving commands from the transmitter and is bound.

If using a Taranis use mode D16 to bind.

`XSR Binding Video <https://www.youtube.com/watch?v=zcsCMYU7--M>`_


Range Check
..............

A pre-flight range check should be done before each flying session. Reflections from nearby metal fences, concrete buildings or trees can cause loss of signal both during range check and during the flight. Follow the steps below to perform the range check.

  1.  Place the model at least 60cm (two feet) above non-metal contaminated ground (e.g. on a wooden bench).
  2.  The receiver antennas should be separated in the model and should not touch the ground.
  3.	The module antenna should be in a vertical position.
  4.  Turn on the transmitter and the receiver, press the F/5 button on the XJT module for 4 seconds to enter range check mode (or use menu on the Taranis), the RED LED will be off, GREEN LED will flash rapidly. The effective distance will be decreased to 1130 (at least 30m).
  5.  Walk away from the model while simultaneously operating the controls on the transmitter to confirm all controls operate normally.
  6.	Press the F/S button on the XJT module for 1-2 seconds to exit range check mode (or disable on Taranis). A steady RED LED indicates normal operation.



Failsafe
..........

.. note::
  For the competition flight it is advisable to turn off the RC failsafes completely and rely on the RFD900x and Pixhawk setup only to deal with RC failures or loss of signal. For flight testing outside of the competition it is recommended to use the RC failsafe as it can add an extra layer of protection if it is configured correctly.
  If failsafe is not set on the Pixhawk and RC the failsafe default will hold the last position before signal was lost. In this case, there is a risk your model will fly away, crash or cause injury. Setting a geofence is also advisable to avoid fly aways.

Failsafe is a useful feature in which all controls move to a preset position whenever the control signal is lost for a period of time. XSR supports failsafe function for all channels. Follow the steps below to sat failsafe positons for each channel:

 1.	Bind the receiver first and turn on both the transmitter and the receiver;
 2.	Move the controls to the desired failsafe position for all channels;
 3. Briefly Press the F/5 button on the receiver (less than 1second). The Green LED will flash twice, indicating the failsafe position has been set in the receiver.

To disable the failsafe function, re-bind the receiver.

.. tip::
  Optionally you can set the RX failsafe to no pulses when it loses signal to the transmitter:
  Turn off the transmitter, power on the receiver and then briefly press the F/S button on the receiver.

FrSky Telemetry
....................

There's also an option to add Telemetry from the Pixhawk to the Taranis LCD screen using the FrSky Receiver.
This works if you connect the RC receiver to the RFD900x or directly to the Pixhawk if you follow these instructions: `FrSky Telemetry <http://ardupilot.org/copter/docs/common-frsky-telemetry.html>`_
