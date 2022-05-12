.. _beamline_operation:

Beamline operation
==================

Login
-----

The wireless PC mouse has a battery saving feature and will turn off after prolonged idle period. The mouse has to switched back on by pressing the power button on the bottom.

This login id and password will be required when re-logging in the computers (e.g., after rebooting the operating system), and can be provided by the beamline staff.

Start EPICS user interface
--------------------------

On the Windows desktop of both computers, users will find a shortcut named “16BMB-PEC Interface”.

This shortcut executes “16BMB_PEC.adl” with necessary options and input parameters. Please keep the options as-written to correctly start the interface.

Attached below is a screen shot of the PEC User Interface.

.. figure:: /images/operation/EPICS_user_interface.png
   :alt: EPICS_user_interface
   :scale: 50 %
   :align: center

It interfaces the control widgets with 16-BM-B station shutters, SR status, EPS status, most demanded
motors for user experiments, intensity monitors with ion chambers and diode, and heater power supply controller and pressure control syringe pump.


EDXD and radiography mode switching
-----------------------------------

Setup of slits and filter for EDXD and radiography measurement, respectively.
Open ‘Slits/Filter Setup’ on the PEC user interface.

.. figure:: /images/operation/slits_filter_interface.png
   :alt: slits_filter_interface
   :scale: 60 %
   :align: center

Input slit sizes and filter setup values in the ‘Preset Position’ window. 

.. warning:: Please do not change other parameters (e.g., Tip X, Y, Z, and so on).

   

Setup 1 is for EDXD measurement and setup 2 is for radiography measurement. Filter value is typically 0 (no filter) for EDXD measurement and -45 (100 μm molybdenum) for radiography measurement. Please close the window after completion.
‘1st Hsize’, ‘1st Vsize’, ‘2nd Hsize’, ‘2nd Vsize’, ‘Filter’ setups change simultaneously by clicking ‘Slit for EDXD’ (EDXD) or ‘For Camera’ (radiography).

.. figure:: /images/operation/slit_mode_switch_interface.png
   :alt: slit_mode_switch_interface
   :scale: 30 %
   :align: center

Radiography measurement
-----------------------
On the PEC user interface,

1.	Click ‘for Camera’ to open slits and to put filter.
2.	Confirm and/or move ‘2TH’ to > 11°.
3.	Move camera IN 

.. figure:: /images/operation/switch_to_radiography_interface.png
   :alt: switch_to_radiography_interface
   :scale: 30 %
   :align: center

Open ‘AVT Vimba Viewer’ on desktop. Check ‘GC1380H’.

Click start to start camera.

To save image, stop camera. File-Save image as.

EDXD measurement
----------------
On the PEC user interface,

1.	Move camera OUT 
2.	Click ‘Slits for EDXD’ to narrow slits and to remove filter.
3.	Move Tip X to IN position 

.. important:: Tip X must be moved to OUT position when putting in and removing PE cell to avoid accidentally bumping the collimator.

EDXD data collation and viewing is done using the :ref:`hpMCA <hpMCA>` software:

1. Open ‘hpMCA’ from shortcut on desktop

.. figure:: /images/hpmca/hpmca_main_screen.png
   :alt: hpmca_main_screen
   :scale: 80 %
   :align: center

2. File -> foreground -> open detector.
3. Click ‘OK’, keeping the default MCA PV name.

4. Find sample Y, Z, and X positions before starting EDXD data collection (cf. page 20-21).

5. Start EDXD data acquisition (Refer to :ref:`hpMCA <hpMCA>` section for EDXD data acquisition and viewing).

.. _bluediamond:

Bluediamond
-----------
The Java-based HPCAT Bluediamond software is a real-time scan viewer program. The user shortcut can be found on the Windows desktop. If the software is started fresh, go to “Configuration” -> “open” to open the input configuration file named “16BMB.txt” in the “C:\\HPCAT Software” directory.  Note that this directory is local, but can be any directory in the network.  The software is straightforward to use and most of the menu items are self- instructing.

Various detectors can be displayed in the scan:

- Beam intensity monitor by ‘Ion Chamber 1’ placed at the entrance of BMB hutch.
- Beam intensity monitor by ‘Ion Chamber 2’ (used only in absorption density measurement).
- Beam intensity monitor by ‘IC2 or Diode’ placed at the downstream of sample. This is mainly used for scanning sample Y and/or Z position by absorption contrast.
- Intensity of ROI in MCA software. This is mainly used for scanning sample X position in EDXD measurement (page 21). 

.. Note:: The labels for these detectors can change based on the names of the ROIs. Bluediamond only refreshes the names for the detectors when it is started. If you change the name of the ROI in hpMCA the names will not be updated in Bluediamond until it is restarted.

To use line cursors (two vertical and two horizontal), select menu Util -> Markers -> Reset. Left and right cursors can be dragged.
The cursor feature is useful for graphical determination of the FWHM and peak center position. You can move sample position by clicking ‘Move’ button at the ‘Center’ in the left column.

.. figure:: /images/operation/bluediamond_interface.png
   :alt: bluediamond_interface
   :scale: 60 %
   :align: center

Sample Y and/or Z positions search
----------------------------------
There are 2 ways to search sample Y and/or Z positions:

(1)	Search by radiography image
(2)	Scan absorption profile


(1)	By radiography image

    - Move to radiography measurement setup (cf. page 8).
    - Narrow slit size to those of EDXD measurement.
    - Mark the narrow slit size and position by tape or something on monitor.
    - Open slit (click ‘for Camera’) for radiography measurement.
    - Move sample position to x-ray beam position shown by a mark on monitor.


(2)	By scan

    - Move to EXDX measurement setup (cf. page 9).
    - Confirm 2TH is >10°.
    - Open ‘Bluediamond’ (:ref:`Bluediamond <bluediamond>` software).
    - Select ‘IC2 or Diode’ in Detector in Bluediamond, uncheck all others.
    - Open ‘scan’ on SAM Y (or Z)

    .. figure:: /images/operation/scan_launch.png
        :alt: scan_launch
        :scale: 45 %
        :align: center

- Set scan parameters of ‘Start’, ‘End’ and ‘#Pts’ (#Pts has to be odd number) (confirm ‘Relative’).

.. figure:: /images/operation/scan_go.png
   :alt: scan_go
   :scale: 100 %
   :align: center

- Click ‘Load&Go’ to start scan.
- Scan results will appear in ‘Bluediamond’ window.

Sample X position scan
----------------------

Sample X position can be adjusted by using intensity of sample or diffraction pattern. However, it is difficult to scan sample X with diffraction intensity of amorphous material. We recommend scanning sample X by using diffraction intensity of MgO ring. Followings are procedures:

- Move Y -1.5 mm from sample Y center to see diffraction patterns of MgO.
- Add ROIs for MgO peaks.
- Then, move Y -1.3 mm position from sample Y center (+0.2 mm Y from -1.5 mm position or move back to the sample Y center and move -1.3 mm Y).
- In order to connect EPICS motor control and MCA software, please click ‘ON’ in ‘Scan1 MCA Trigger Toggle’, and then input data acquisition time for each step in ‘Preset Real Time’ (typically, 2-5 second).
- Open ‘Scan’ in ‘SAM X’, and input parameters (typically, Start=-1, End=1, #Pts=21).
- Then, click ‘Load&Go’ to start scan.
- Sample X center is the location where MgO diffraction intensity is the minimum.

.. note:: After the scan, please do not forget to ‘OFF’ ‘Scan1 MCA Trigger Toggle’, and input 0 in ‘Preset Real Time’.

.. figure:: /images/operation/mgo_scan.png
   :alt: mgo_scan
   :scale: 80 %
   :align: center

.. figure:: /images/operation/scan_trigger.png
   :alt: scan_trigger
   :scale: 30 %
   :align: center

Liquid/amorphous structure measurement
--------------------------------------
A python program ‘multiangle.py’ is available for automatic data acquisition of EDXD pattern with varying 2θ angle.

- Open the python program by running ‘multiangle.bat’ from the desktop shortcut.

.. figure:: /images/operation/multiangle_setup.png
   :alt: multiangle_setup
   :scale: 80 %
   :align: center

You have the following 3 options:

1.	Create a new setup automatically by clicking Setup in main window. In the pop-up window enter desired q-range and usable E range, and % overlap for the measurements. The built in algorithm will calculate optimal 2theta angles and populate the main window.

.. figure:: /images/operation/multiangle_automatic.png
   :alt: multiangle_automatic
   :scale: 100 %
   :align: center

2.	Load previously saved setup, click Load in main window
3.	Add 2-theta angles manually by clicking Add in the main window for each angle.

Adjust the slit sizes and exposure times for each 2-theta 

Input parameters:

    1.	2θ = 2theta angle
    2.	1stV = 1st slit Vertical size
    3.	1stH = 1st slit Horizontal size
    4.	2ndV = 2nd slit Vertical size
    5.	2ndH = 2nd slit Horizontal size
    6.	Det.V = Detector slit Vertical size
    7.	Det.H = Detector slit Horizontal size
    8.	Exp. (s) = Data collection time in ‘Live time’ (i.e. Actual data acquisition time is Live time + Dead time)

If you want to repeat measurement, you can set ‘Iterations = 2 or higher.

.. important:: Confirm the following: 

   - ‘Camera Vpos’ = 110 ‘Beamstop’ = OUT ‘Tip X’ = 0
   - ‘Scan1 MCA Trigger Toggle’ = OFF (nothing in line 2) Both ‘Preset Real Time’ and ‘Preset Live Time’ = 0
   - Slit and Filter setup is ‘EDXD’ condition (‘Filter’ = 0, slit size is small) ‘position of sample is correct’.

Then, please make dummy saved file in hpMCA:

* File -> Save As (please make a dummy file with suffix ‘_000’, file extension will be .hpmca)
* Open File -> Preferences
* In preferences, please check ‘yes’ for ‘autosave when acquisition stopped’. (hpMCA will save file for each angle data with the name suffix of ‘_001’, ‘_002’...).

Then, to start multiangle measurement, 

- On Multiangle control window, click Run 

.. Note:: After finishing the Multiangle collection, please do not forget to check ‘no’ for ‘autosave when acquisition stopped’.

If you want to stop the Multiangle measurement, click Stop.

Increase pressure
-----------------
The PEC oil pressure is controlled by the Teledyne ISCO 30D dual syringe pump system. 
The maximum pressure allowed is 14,000 psi (9,000 psi for ultrasound or grooved cells).
Syringe pump is controlled through the MEDM interface

.. figure:: /images/operation/syringe_pump_interface.png
   :alt: syringe_pump_interface
   :scale: 29 %
   :align: center

Basic pump operation
Procedure for increasing, maintaining, and decreasing pressure.

Compression:

1. Make sure Mode is selected as “Compress”. (Mode button is hidden while Pressure Control is in “Run” state). Stop the Pressure Control before switching Mode.
2. Refill pumps A and B (click the button Refill for each pump). Wait until both pumps finish refilling.
3. Set Max flow for both pumps to 5ml/min.
4. Set the Oil pressure setpoint to 20 psi.
5. Set Pressure control to Run. Pump will go through the initial equalization sequence; this will take around 30 seconds to one minute. Pressure may go up to ~80 psi and fluctuate somewhat during this process. Wait until the Actual oil pressure stabilizes at 20 psi.
6. Increase the Oil pressure setpoint to your required pressure (maximum allowed is 14,000psi). Pump will gradually reach the setpoint pressure and maintain the pressure continuously. 
7. If you don’t want the pump to maintain the pressure continuously after reaching the setpoint, set the Maximum oil flow-rates for pumps A and B to 0.0001 ml/min. DO NOT switch Pressure Control to Stop. 
8. To reach the next oil pressure setpoint, re-enable pressure control by setting Max flow rates back to 5 ml/min.

Decompression:

1. Set Pressure Control to Stop.
2. Set Mode to Decompress. (Note: due to problem in the current version of the controller software, sometimes communication with the pump during this step, the indicators colors can change to white. If this happens, please wait around 30 seconds, the communication should get re-established on its own. Afterwards, you may need to toggle back and forth between Compress and Decompress, make sure Decompress in finally selected). 
3. Set Pressure Control to Run.
4. Wait around 1 minute before doing anything else. After around 30 seconds, one of the pumps (A or B) will start emptying out. Wait until the level in that pump reaches around 7.5 ml.
5. Set the setpoint pressure to 20 psi.
6. After the actual oil pressure is at 20 psi, switch pressure control to Stop.
7. Open the valves to vent the remaining oil pressure.


Heating
-------
Before connection of cable, please confirm ‘Power Output’ in ‘PEC User Interface’ is ‘OFF’.

.. figure:: /images/operation/heating_power_on.png
   :alt: heating_power_on
   :scale: 30 %
   :align: center

In hutch, please confirm ‘Heater Output Control Switch’ is ‘Disabled’.

- See that the thick power cables are connected. 

.. figure:: /images/operation/heating_cable_connections.png
   :alt: heating_cable_connections
   :scale: 40 %
   :align: center

- Turn On a fun on PE press for cooling of press body.

- ‘Enable’ on the ‘Heater Output Control Switch’.


- Before starting heating, it is recommended to start ‘Stripchart’ to save log of heating (cf. page 26 about Stripchart).

On ‘PEC User Interface’,

1.	At first, please confirm ‘Voltage’ ‘Set Point (V)’=0, ‘Setpoint (Watt) on PID control = 0, and ‘Over Protection’ is ON.
2.	‘Power Output’ ON
3.	Input 200 in ‘Limit’ under ‘Current’. Please input again even if the value is 200.
4.	Click ‘Clear fault’.
5.	‘PID ON/OFF’ ON
6.	Tweak ‘Setpoint (Watt)’ by 1 W to 3 W.
7.	Check ‘Readback (Watt)’ is responding, and ‘Resistance’ is lower than 0.1 (typically, ~0.04-0.05 at ~1 W).

.. Note:: Response of heater is slow particularly at <10W. Please wait a while.

.. important:: Increase of ‘Readback (Watt)’ may stop at <3W. If so, please check ‘Measured (Amp)’ under ‘Current’. If  ‘Measured (Amp)’ value is 2.65, it is likely to forgot the procedure 3 (Input of 200 in ‘Limit’ of ‘Current’). In this case, please lower ‘Setpoint (Watt)’ to 0, turn OFF the ‘PID ON/OFF’, input 0 in Set Point (V), and turn Off the ‘Power Output’. Then, please restart the procedures.

8.	If heater response and resistance is okay, increase ‘Setpoint (Watt)’ slowly (it is better to keep <5 difference between ‘Readback (Watt)’ and ‘Setpoint (Watt).).

Cooling can be done by

    (1) slow cooling by gradually decreasing ‘Setup (Watt)’ to 0, or 
    (2) Turn OFF ‘Power Output’ to quench sample.

In both cases, after cooling,

- Input 0 in ‘Setup (Watt)’.
- ‘PID On/OFF’ OFF
- ‘Power Output’ OFF
- Input 0 in ‘Set Point (V) under ‘Voltage’.

- ‘Disable’ on the ‘Heater Output Control Switch’.

.. warning:: Do not touch on press at least until turning off the power of heater power supply. Even after the power off, please take care. If you heated more than 1000 °C for more than several hours, press body may be hot. Please wait a while to cool down press body.

After cooling of press body, please remove heating cables.


Data logging
------------

Program **Log book** saves compression and heating records with time. Log book allows recording any process variable (PV)

- Open ‘Log book’ from desktop shortcut.
