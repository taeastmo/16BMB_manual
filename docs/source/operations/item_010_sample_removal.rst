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
   Clicking on the shortcut will launch a software package that allows the Aerotech rotation stage underneath the PE press to be deactivated. While active, a small amount of holder current keeps the rotation stage at its      set position. However, the holding current is not enough to withstand the torque required to force the bottom piston of the PE press to its starting position after an experiment, and will thus throw an overcurrent fault    if not deactivated before resetting the piston of the press. To avoid this unnecessary fault, the holding current of the rotation stage can be deactivated as follows. 

   2. Once the Automation1 software menu is visible, ensure the :guilabel:`639171-1-1 Loaded` box is selected and click :guilabel:`Connect`. 

.. figure:: /images/sample_removal/automation1_connect.png
   :alt: automation1_connect
   :width: 720px
   :align: center

| 
After connecting to the rotary stage controller, locate the toggle switch found in the bottom lefthand corner of the control screen. Click the toggle to deactivate the rotation stage motor. Once this is completed, there will be no holding current applied to the rotary stage and the PE press can be rotated freely by hand. 

.. figure:: /images/sample_removal/automation1_axis_enabled.png
   :alt: automation1_axis_enabled
   :width: 720px
   :align: center
.. figure:: /images/sample_removal/automation1_axis_disabled.png
   :alt: automation1_axis_disabled
   :width: 720px
   :align: center






   1. Make sure Mode is selected as “Compress”. 

   .. note:: Stop the Pressure Control before switching Mode. (Mode button is hidden while Pressure Control is in “Run” state). 

   2. Refill pumps A and B (click the button :guilabel:`Refill` for each pump). 

   .. note:: Wait until both pumps finish refilling.

   3. Set Max flow for both pumps to 5ml/min.
   #. Set the Oil pressure setpoint to 20 psi.
   #. Set Pressure control to Run. Pump will go through the initial equalization sequence; this will take around 30 seconds to one minute. 

   .. note:: Pressure may go up to ~80 psi and fluctuate somewhat during this process. 
      Wait until the Actual oil pressure stabilizes at 20 psi.

   6. Increase the Oil pressure setpoint to your required pressure (maximum allowed is 14,000psi). Pump will gradually reach the setpoint pressure and maintain the pressure continuously. 
   #. If you don't want the pump to maintain the pressure continuously after reaching the setpoint, set the Maximum oil flow-rates for pumps A and B to 0.0001 ml/min. 

   .. important:: DO NOT switch Pressure Control to Stop. 

   8. To reach the next oil pressure setpoint, re-enable pressure control by setting Max flow rates back to 5 ml/min.

Subsection 2
^^^^^^^^^^^^^

   1. Set Pressure Control to Stop.
   2. Set Mode to Decompress. 
   3. Set Pressure Control to Run.

   .. important:: Wait around 1 minute before doing anything else. 
      After around 30 seconds, one of the pumps (A or B) will start emptying out (there will be a valve opening/closing sound). 
      Wait until the level in that pump reaches around 7.5 ml.

   4. Set the setpoint pressure to 20 psi.
   #. After the actual oil pressure is at 20 psi, switch pressure control to Stop.
   #. Open the valves to vent the remaining oil pressure:

      1. Open valve control from the main PEC interface menu "Pump control menu"

      .. figure:: /images/sp/valve_control_2.png
         :alt: valve_control
         :width: 300px
         :align: center

      2. Toggle Valves 1-4 to Low. 

      .. note:: If the readback text for a valve is high (red), and pressed button is low: click the :guilabel:`high` button and then the :guilabel:`low` button.

      .. note:: If the valve 1-4 buttons are hidden check the following conditions are met: 
         
         * Pressure : <= 20psi
         * Pressure setpoint: 20psi
         * Pressure control: stopped

   .. figure:: /images/sp/valve_control_blocked.png
       :alt: valve_control_blocked
       :width: 300px
       :align: center


