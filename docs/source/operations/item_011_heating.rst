.. _Heating_control:

Heating control
---------------

.. important:: To heat samples under high pressure, a 10 V, 265 amp TDK power supply is used to pass current through a cylindrical graphite heater inside the sample cell. For safe operation of the power supply, an interlock system with an indicator light is provided to prevent output of electrical current while experimentalists are inside the hutch. While the voltage rating of the power supply is relatively low, its rated current output is high and could result in arcing if a wrench or other metal object short circuits the path between the PE anvils. Please read the following procedure carefully.

An interlock switch is located on the experimental table to the immediate right of the PE press. The color of the indicator light can be green, yellow, or red, depending on the status of the interlock switch and the output state of the TDK power supply. The figure below illustrates all three states. A green light indicates that the switch has been toggled to activate the interlock feature, which prevents The TDK from outputting any current. A yellow light indicates that the interlock feature is deactivated and the TDK output is off. In this case, the yellow light warns of a potential hazard--current could be supplied to the PE press while an experimentalist is loading samples, connecting cooling lines, etc. if the TDK output is inadvertently activated by a second experimentalist. Finally, a red indicator light means that the interlock is deactivated and the TDK is outputting current to the PE press! 


.. figure:: /images/operation/TDK_interlock_diagram.png
   :alt: TDK_interlock_diagram
   :width: 600px
   :align: center


Before connection of cable, please confirm 'Power Output' in 'PEC User Interface' is 'OFF'.

.. figure:: /images/operation/heating_power_on.png
   :alt: heating_power_on
   :width: 600px
   :align: center

In hutch, please confirm 'Heater Output Control Switch' is 'Disabled'.

   1. See that the thick power cables are connected. 

   .. figure:: /images/operation/heating_cable_connections.png
      :alt: heating_cable_connections
      :width: 600px
      :align: center

   2. Turn On a fun on PE press for cooling of press body.

   3. 'Enable' on the 'Heater Output Control Switch'.


   4. Before starting heating, it is recommended to start ':ref:`LogBook <logbook>`' to save log of heating. 

On 'PEC User Interface',

   1.	At first, please confirm 'Voltage' 'Set Point (V)'=0, 'Setpoint (Watt) on PID control = 0, and 'Over Protection' is ON.
   2.	'Power Output' ON
   3.	Input 200 in 'Limit' under 'Current'. Please input again even if the value is 200.
   4.	Click :guilabel:`Clear fault`.
   5.	'PID ON/OFF' ON
   6.	Tweak 'Setpoint (Watt)' by 1 W to 3 W.
   7.	Check 'Readback (Watt)' is responding, and 'Resistance' is lower than 0.1 (typically, ~0.04-0.05 at ~1 W).

   .. Note:: Response of heater is slow particularly at <10W. Please wait a while.

   .. important:: Increase of 'Readback (Watt)' may stop at <3W. If so, please check 'Measured (Amp)' under 'Current'. If  'Measured (Amp)' value is 2.65, it is likely to forgot the procedure 3 (Input of 200 in 'Limit' of 'Current'). In this case, please lower 'Setpoint (Watt)' to 0, turn OFF the 'PID ON/OFF', input 0 in Set Point (V), and turn Off the 'Power Output'. Then, please restart the procedures.

8.	If heater response and resistance is okay, increase 'Setpoint (Watt)' slowly (it is better to keep <5 difference between 'Readback (Watt)' and 'Setpoint (Watt).).

Cooling can be done by

    (1) slow cooling by gradually decreasing 'Setup (Watt)' to 0, or 
    (2) Turn OFF 'Power Output' to quench sample.

In both cases, after cooling,

   #. Input 0 in 'Setup (Watt)'.
   #. 'PID On/OFF' OFF
   #. 'Power Output' OFF
   #. Input 0 in 'Set Point (V) under 'Voltage'.

   #. 'Disable' on the 'Heater Output Control Switch' in the hutch.

   .. danger:: Do not touch on press until turning off the power of heater power supply. 
      Even after the power off, please take care. 
      If you heated more than 1000 °C for more than several hours, press body may be hot. 
      Please wait until the press body is cool.
