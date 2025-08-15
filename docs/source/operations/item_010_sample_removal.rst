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

.. warnining:: Do not attempt to turn the breech until the valves of the syringe pump, including the line valve, have been opened. This should have already been completed, but review :ref:`Pressure control <Pressure_control>` if this step was skipped for some reason.

Lowering the PE press piston
^^^^^^^^^^^^^^^^^^^^^^^^^^^^








