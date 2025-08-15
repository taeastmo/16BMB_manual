Sample Removal Procedure
------------------------
Due to several changes following the APS-Upgrade, users must adhere to the following procedure to safely remove their samples and reset the PE press for the next sample. 

.. warning:: Failure to follow these instructions can lead to damage of beamline equipment and loss of experimental time.

Sample Removal
^^^^^^^^^^^^^^
1. After following the decompression steps outlined in :ref:`Pressure control <Pressure_control>` as well as the steps to disable and interlock the heater power supply as explained in :ref:`Heating control <Heating_control>`, find the "Automation1" shortcut on the desktop of the beamline control computer:

.. figure:: /images/sample_removal/automation1_shortcut.png
   :alt: automation1_shortcut
   :width: 720px
   :align: center
|

Clicking on the shortcut will launch a software package that allows the Aerotech rotation stage underneath the PE press to be deactivated. While active, a small amount of holder current keeps the rotation stage at its     set position. However, the holding current is not enough to withstand the torque required to force the bottom piston of the PE press to its starting position after an experiment, and will thus throw an overcurrent fault if not deactivated before resetting the piston of the press. To avoid this unnecessary fault, the holding current of the rotation stage can be deactivated as follows. 

2. Once the Automation1 software menu is visible, ensure the :guilabel:`639171-1-1 Loaded` box is selected and click :guilabel:`Connect`. 

.. figure:: /images/sample_removal/automation1_connect.png
   :alt: automation1_connect
   :width: 720px
   :align: center

|

3. After connecting to the rotary stage controller, locate the toggle switch found in the bottom lefthand corner of the control screen. Click the toggle to deactivate the rotation stage motor. Once this is completed, there will be no holding current applied to the rotary stage and the PE press can be rotated freely by hand. 

.. figure:: /images/sample_removal/automation1_axis_enabled.png
   :alt: automation1_axis_enabled
   :width: 720px
   :align: center
.. figure:: /images/sample_removal/automation1_axis_disabled.png
   :alt: automation1_axis_disabled
   :width: 720px
   :align: center

|

4. Enter the hutch and rotate the PE press counterclockwise to align the hole of the lock with the locking pin.

.. important:: Please ensure the collimator tip is in the "out" position to avoid bumping the tip. If the tip is bumped, realignment can take several hours by the beamline staff.

.. figure:: /images/sample_removal/PE_press_rotated.png
   :alt: PE_press_rotated
   :width: 720px
   :align: center

|

5. Raise the locking pin into the lock with the socket head cap screw and secure the pin by dropping the screw into the retaining groove.

.. figure:: /images/sample_removal/aerotech_locking_sequence.png
   :alt: aerotech_locking_sequence
   :width: 720px
   :align: center

|

6. Once the PE press is locked into place, used a crescent wrench to loosen the breech and gently force the top anvil to break away from the sample assembly. Carefully back out the breech until there is sufficient space to remove the sample cell. 

.. warning:: Do not attempt to turn the breech until the valves of the syringe pump, including the line valve, have been opened. This should have already been completed, but review :ref:`Pressure control <Pressure_control>` if this step was skipped for some reason.

Lowering the PE press piston
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. important:: This process takes patience and cannot be rushed with "brute force." The friction between the hydraulic line and oil prevents rapid movement of the piston, and trying to rush the process only increases the chances that the crescent wrench will slip off of the breech and collide with the collimation tip or the pre-sample slits.

After removing the sample, the bottom piston of the PE press needs to be lowered to allow sufficient travel for compression of the next sample. 
1. With the PE press rotation locked, place the plastic spacer block in between the two anvils.
2. Ensure all syringe pump valves are open, including the line valve.
3. Turn the breech clockwise with a crescent wrench to drive the piston down.
4. Close the line valve of the syrine pump to prevent the piston from raising again due to the weight of the hydraulic oil in the line.

.. figure:: /images/sample_removal/PE_piston_reset.png
   :alt: PE_piston_reset
   :width: 720px
   :align: center











The syringe pump is now located on the 16BMB hutch roof, which puts the hydraulic oil reservior and majority of the hydraulic line above the height of the PE press. The potential energy of the line  







