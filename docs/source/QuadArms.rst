Quad Arms
----------

Parts Required

 * CF Bar 15x3mm
 * CF Motor Mount Left
 * CF Motor Mount Right
 * CF Middle Left
 * CF Middle Right
 * CF Undermount
 * 2x 25mm and 2X 40mm M4 screws and 4x M4 locking nuts

..Note::
  You will require two complete quad arms for the Mozzie. The front and rear quad arms are mechanically identical, however the ESC motor direction setting needs to match the diagram in the System Check section.


Step 1 - Soldering the Motor and ESC
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.... image:: images/QuadArmSolder_sm.jpg
        :target: images/QuadArmSolder.jpg

Because of the compact lightweight design of the quad arms some care must be taken with their construction and assembly.
Their disassembly only requires the removal of the heatshrink and the motor screws.

An important step is to ensure that the length of the three cables between the ESC and the Motor is accurate.
Making it two short will mean the ESC will be mounted to far out on the quad arm, and making it to long will mean that the cables won't fit under the heatshrink neatly.

..Tip::
  If preferred one can assemble the quad arm parts first, using steps 2 and 3 below, to use the quad arms as a template to find the correct cable lengths.

Solder a male XT30 plug to the red and black cables of the ESC ensuring the correct connector polarity. (Red + Black -) Don't forget to place the heat shrink on the cable first.

Then cut the three black cables from the ESC and the three black cables from the motor both to a length of XXmm.
Make sure the total length of cable between the ESC and motor is what is required when mounted to the arm and remove about 8mm of insulation from each cable so that these sections overlap.
Then place a piece of heatshrink over each cable and solder the ESC cables to the respective motor cable so that the cables do not cross each other. (The motor direction will be determined by the ESC setting later)

Use the hot air gun to carefully heatshrink each solder joint.

..Tip::
  The hot air gun can be very hot, be careful not to hold in one place for very long and gradually go along the length of the heatshrink until it becomes taught around the cables or connector.
  Avoid heating the ESC and motors directly for prolonged periods. Keep hands and flammable items well clear! (including the aircraft foam parts!!)



Step 2 - Mounting the 3D Printed parts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

..Caution::
  Carbon Fiber dust and particles can be potentially harmful. Do not inhale and use protective gloves in a well ventilated area to cut and work on the CF Bar.

..Note::
  Not all 3D parts come off the printer in perfect condition. Before assembling any 3D printed parts, or gluing any 3D printed parts ensure that the parts all fit together
  by carefully removing any excess plastic from the print and seeing if they dry fit together first!


Use a fine tooth metal saw to carefully cut the CF Bar into two 400mm long pieces. Try to cut the CF cleanly all the way through using the saw so it does not splinter,
then carefully file the cut edges smooth to allow for an easier fit.
Mark the middle of each CF bar and test that the 3D printed parts fit onto the CF bar correctly with tight tolerances.
Use the middle mark to align the middle pieces symmetrically and use the end of the CF bar to position the motor mount pieces.

..Tip::
  Make sure the pieces all have the correct orientation and that the 3D printed Motor Mounts are on the correct side of the CF bar.
  The screw hole layout on the motor mount is determined by where the cables exit the motor so that they can run along the CF bar to the fuselage.


.... image:: images/QuadArmDry_sm.jpg
        :target: images/QuadArmDry.jpg


Then remove the 3D motor mounts and dry test fit the quad motors onto them.

..Warning::
  Before screwing the motors onto the mounts make sure that the screws used to attach the motor mounts and CF Bar are the correct length! Screws that are too long will damage the motor windings!
  Screws that are too short will not hold the motors for prolonged use. Please use screws that just make it through the motor's lower aluminum plate (ideally by about 0.5-1mm).
  It's advisable to use washers to underneath the screw heads to distribute the forces and adjust the length as required.

Step 3 - Drilling the Motor Mount
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The 3D printed motor mounts are intentionally angled forwards so that the Mozzie has a pitch up wing angle of attack in the wind.
To make sure the motor is mounted correctly it is necessary to drill the screw holes through the CF bar on an angle, the hole angle should be 90 degrees to the top surface of the 3D motor mount.

..Tip::
  Try not to use to much force when the drill is nearly through the CF to avoid it splintering.
  Use the left over piece of CF bar to practice drilling.

Slide the all 3D printed parts onto the CF bar as shown in Step 1, into the desired location with the correct orientation and placement.
Use a sacrificial 3D printed motor mount or timber wedge with the right angle as follows to get the correct drill angle, and then very slowly drill Xmm holes using a drill press if possible.

.... image:: images/QuadArmDrill_sm.jpg
        :target: images/QuadArmDrill.jpg

After cleaning the newly drilled holes, carefully screw the motors onto the mounts and CF bar, and check to see if the motors can spin freely.

Step 4 - Arm Assembly
^^^^^^^^^^^^^^^^^^^^^^^^^^

Once all the motor tolerances are checked take off the motors and check all the components before assembly.
Slide the heatshrink over the CF bar then use loctite on the screws to mount the motors permanently.
Align the cables and ESC along the CF bar and try to keep the cables to the front edge of the CF bar and then use a hot air gun to heatshrink them in place.

The finished quad arm should look like this:

.... image:: images/QuadArmFinish_sm.jpg
        :target: images/QuadArmFinish.jpg

..Tip::
  The hot air gun can be very hot, be careful not to hold in one place for very long and gradually go along the length of the heatshrink until it becomes taught around the Quad arm.
  Avoid heating the ESC and motors directly for prolonged periods. Keep hands and flammable items well clear!

Step 5 -  Attaching the Quad Arms to the Fuselage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The final step for the quad arms section is to attach them correctly to the completed Mozzie fuselage.

Place a mark on the fuselage 12mm behind the fuselage hatch. Then dry fit the quad arm on the rear mark and into the front nose crease as per the picture below.
Mark the screw holes and rectangular cable penetrations on the 3D printed middle mounts onto the fuselage.
Carefully cut the foam all the way through to the inside of the fuselage so that the cables can be routed internally to the power loom,
and that the servo cables can be routed to the Pixhawk from the quad arms.

.... image:: images/QuadArmComplete_sm.jpg
        :target: images/QuadArmComplete.jpg

Place the M4 locking nuts into the undermount and insert the screws through the quad arm and then through the fuselage.
Use the 20mm long M4 screws for the front quad arm and the 30mm M4 screws for attaching the rear quad arm.

Place the 3D printed Undermount into the fuselage directly under the quadarms and then loosely screw it together until the screws are attached to the nuts.
Then route all the ESC cables through their respective penetrations and carefully screw the quadarms in place without damaging the cables.

Make sure to align the quadarms and only tighten the arms so they cannot move around loosely on the foam fuslage.
Be careful not to overtighten the screws as this will over fatigue the foam and make it structurally unstable.

..Tip::
  Check at every pre-flight, and in particular after any hard landing (crash), that the quad arms do not have excessive movement and tighten as required.
