Full Systems Check
===================

Finish Build
------------

Set control surface and Loctite control horn screws!
Cut hole in foam lid for Borroca Tube!



  - CoG is on the main forward wing spars, typically I make it about 3mm nose heavy for good tail control
  - Placing a smaller battery in the nose is fine provided it can support the max quad/transition current draw (60-120A), laying it down might get the battery into the nose more to get the correct CoG. Adding ballast (big washer's etc) into the nose works as well so long it's secured there and can't roll pass the battery. CoG is sensitive, and although it is identical for both winged and quad flight, it will easily take off in quad mode with the wrong CoG, but will result in a crash on          transition to forward flight. It's good practice to check the CoG every preflight
  - Disable the airspeed in parameters if you want to fly without it.
  - With quad assist enabled I'd recommend disabling stall prevention for better flight control.
  - As discussed don't connect a current sensor between the battery and main cable loom unless this is rated for over 150A (which most are not). Rather connect this between the rear Xt60 and the forward motor ESC. Power is provided to the PXH/servo's via ubec so the current/power module is optional/redundant. Also the pi has a soldered power cable that can be connected to the PXH USB JST port for third power redundancy. Plug this in as required.
  - Transitioning to qloiter from a forward flight mode is possible but not recommended. Transition to qhover first then 5-10 seconds later to qloiter, to avoid the aircraft using the quadmotors frantically trying to position hold wilst still moving forwards. Chk the quad arms are secured/rigid on the fuselage prior to every flight. The quad arms can become loose after a rough landing.
  - The forward motor does not have ESC prop braking activated. Landing on hard surfaces might cause a spinning forward motor to strike the ground on landing which can damage the prop. (the aeronaut prop has fragile tips, which doesn't help)
  - Use forward assist and wind feathering if operating as a quad in high winds.

Tuning
------

  Add most important tuning items and values in table.

Comms Setup
-----------

 Add Comms setup info like IP and Channels etc
