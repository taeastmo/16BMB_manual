.. _Heating_control:

Heating control
---------------

.. important:: To heat samples under high pressure, a 10 V, 265 amp TDK power supply is used to pass current through a cylindrical graphite heater inside the sample cell. For safe operation of the power supply, an interlock system with an indicator light is provided to prevent output of electrical current while experimentalists are inside the hutch. While the voltage rating of the power supply is relatively low, its rated current output is high and could result in arcing if a wrench or other metal object short circuits the path between the PE anvils. Please read the following procedure carefully.

An interlock switch is located on the experimental table to the immediate right of the PE press. The color of the indicator light can be green, yellow, or red, depending on the status of the interlock switch and the output state of the TDK power supply. The figure below illustrates all three states. A green light indicates that the switch has been toggled to activate the interlock feature, which prevents The TDK from outputting any current. A yellow light indicates that the interlock feature is deactivated and the TDK output is off. In this case, the yellow light warns of a potential hazard: current could be supplied to the PE press while an experimentalist is loading samples, connecting cooling lines, etc. if the TDK output is inadvertently activated by a second experimentalist. Finally, a red indicator light means that the interlock is deactivated and the TDK is outputting current to the PE press! 


.. figure:: /images/operation/TDK_interlock_diagram.png
   :alt: TDK_interlock_diagram
   :width: 600px
   :align: center



.. figure:: /images/operation/TDK_heating_controls_menu.png
   :alt: TDK_heating_controls_menu
   :width: 700px
   :align: center


If you need to heat your sample during your experiment, the procedure is as follows:

   1. Flip the interlock switch down so the indicator light turns green.
   2. See that the thick power cables are connected to the press.

   .. figure:: /images/operation/heating_cable_connections.png
      :alt: heating_cable_connections
      :width: 600px
      :align: center

   3. Ensure that the water cooling lines are connected.
   4. Turn on and position the fan to cool the PE press body.
   5. Before leaving the hutch, flip the toggle switch on the interlock so the light turns yellow.
   6. Compress the sample to the desired pressure.
   7. On the beamline control sceen, click :guilabel:`HEATING` to bring up the TDK power supply control screen.
   8. Before starting heating, it is recommended to start a strip chart to save log of heating. Instructions for this are included in the "General Data Logging" section of this manual.

Once the heater control screen is open, follow these steps:

   1. Before beginning heating, ensure that the PID power setpoint and voltage setpoint are set to zero. 
   2. Input '8' in the voltage protection and limit setpoint fields. 
   3. Input '200' in the current limit field. Please input again even if the value is 200. 
   4.	Click :guilabel:`Clear fault`.
   5. Turn on the PID controller (with the setpoint still at 0).
   6. Enable the power output.
   7. Set the PID to 1-2 W. The voltage will start to increase by 0.001 V at a time. When the voltage reaches ~0.035 V (depending on the resistance of the sample cell), the TDK will begin outputting current and the PID should have good control over the power supply. 
   8. Check that 'Readback (Watt)' is responding, and 'Resistance' is lower than 0.1 (typically, ~0.04-0.05 at ~1 W).
   9. If heater response and resistance is okay, increase 'Setpoint (Watt)' slowly (it is better to keep <5 difference between 'Readback (Watt)' and 'Setpoint (Watt).).
 
.. Note:: Response of heater is slow particularly at <10W. Please wait a while.


.. Note:: The PID controller will take care of the current output. Never change the value shown in the current setpoint field, either during or before heating.


.. Warning:: If you fail to set BOTH the PID power setpoint and voltage setpoint to zero before beginning heating, you run the risk of instantly applying a large amount of current to the press and subsequently destroying the graphite heater. Even if the PID power setpoint is zero, a non-zero value of voltage will cause the heater to output some amount of current (often a very large value), before slowly trying to back the voltage and current down to the PID power setpoint. 
  

Cooling can be done by

    (1) slow cooling by gradually decreasing 'Setup (Watt)' to 0, or 
    (2) Turn OFF 'Power Output' to quench sample.

In both cases, after cooling,

   #. Input 0 for the PID power setpoint.
   #. 'PID On/OFF' OFF
   #. 'Power Output' OFF
   #. Input 0 in 'Set Point (V)' under 'Voltage'.
   #. Toggle the interlock switch so the light turns green.

.. danger:: Do not touch the press until disabling the power supply output and enabling the interlock switch in the hutch. Even after the power is off, please take care. If you heated more than 1000 °C for more than several hours, the press body may be hot. Please wait until the press body is cool.
