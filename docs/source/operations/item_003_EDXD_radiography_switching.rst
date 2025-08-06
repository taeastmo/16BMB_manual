EDXD and radiography mode switching
-----------------------------------
There are currently three modes of operation:

1. EDXD with direct (collimated) beam
2. EDXD with condensed beam 
3. Radiography imaging with direct beam

Direct beam mode delivers a collimated beam for EDXD diffraction measurements. The size of the beam can be adjusted by varying the sizes of the incident slits, with a typical size being 100 (H) x 300 (V) μm. If the user desires higher flux, the condensed beam mode can be used to focus 1 mm of beam in the horizontal direction down to 20 μm (typical vertical size remains at 300 μm). This provides roughly 7.5x the on-sample flux as compared to using the collimated beam. Finally, radiography measurements can be acheived with a large collimated beam, typically 1 x 1 mm. This page provides instructions on setting up each mode and switching between modes during the experiment.

| To setup slit sizes, positions, filter, etc. for the desired mode(s), click on the menu button :guilabel:`Mode Setup` on the PEC user interface.

.. figure:: /images/operation/mode_setup_menu.png
   :alt: mode_setup_menu
   :width: 720px
   :align: center

To set up direct and/or condensed beam modes for EDXD, select :guilabel:`Direct to Condensed` from the Mode Setup menu. This will bring up a menu with various parameters to customize each mode.

.. figure:: /images/operation/direct_2_condensed_mode.png
   :alt: direct_2_condensed_mode_setup
   :width: 500px
   :align: center

Generally, these parameters should only be set by the beamline staff, as they are based on careful alignment and calibration of the beamline. Please talk to beamline staff if you need them changed for any reason. After 
the parameters are set, pressing :guilabel:`GO` under either beam mode will move motors to their respective preset positions. 



| Setup of slits filter for direct beam EDXD and radiography measurement.
| Click on the menu button :guilabel:`Mode Setup` on the PEC user interface and open the option :guilabel:'EDXD to radiography'.

.. figure:: /images/operation/slits_filter_interface.png
   :alt: slits_filter_interface
   :width: 500px
   :align: center

Input slit sizes and filter setup values in the 'Preset Position' window. 

.. warning:: Please do not change other parameters (e.g., Tip X, Y, Z, and so on).

   

Setup 1 is for EDXD measurements and setup 2 is for radiography measurement. Filter value 
is typically 0 (no filter) for EDXD measurement and -45 (100 μm molybdenum) for 
radiography measurement. Please close the window after completion.
'1-st Hsize', '1-st Vsize', '2-nd Hsize', '2-nd Vsize', 'Filter' setups change 
simultaneously by clicking :guilabel:`Slit for EDXD` (EDXD) or :guilabel:`For Camera` (radiography).

.. figure:: /images/operation/slit_mode_switch.png
   :alt: slit_mode_switch
   :width: 720px
   :align: center
